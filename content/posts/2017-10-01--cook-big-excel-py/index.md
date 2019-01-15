---
title: Cooking big Excel files with Python and Openpyxl
category: "python"
cover: python-hello-world.png
author: Shawon Ashraf
---

At least once in life, every computer user has to handle some spreadsheets or, excel files. Sometimes to put formulas in for accounting stuff, sometimes to store data from Google forms or other surveys and etc. So what do you actually do when the spreadsheet contains just survey data or no number to apply formulas at all? I know you'll get your hands dirty and do it manually. It's fine if the there's data from roughly a hundred people. What will you do if there's data from a thousand or more? I'd have run away in such cases because I'm way too lazy to scroll down and have a look at those. Hopefully I know how to do magic tricks using Python and I'm going to show you this specific magic trick today.

> **Let's make a problem first**

I have a spreadsheet at my hand that has Name, Address and E-mail of 10,000 (Ten thousand, read that aloud) people. What I need to do is using this information I need to create .txt files for each of them using their names as the file name that'll contain there Name, Address and E-mail. More like a business card.

**[ I generated the data in the file using Faker module, all data is fake ]**

A screenshot of a portion of the file for your reference :

<img src="http://i.imgur.com/2WSIXMt.png" alt="cook-big-excel-py-1" width="720"/>



> **What we need**

- ```python3```
- ```openpyxl``` Module. Install it using the following command in your command prompt / shell:
```bash
pip install openpyxl
```
- A text editor of your choice : Atom, VS Code, Sublime, Emacs, Vim whatever you like.



> **So let's get to code**

Our spreadsheet file name is : **TestBook.xlsx**

[ All files and code is on this github repo link](https://github.com/ShawonAshraf/OpenpyxlBlogPost)


```python
import openpyxl as opx

fileName = '../excelFile/TestBook.xlsx'
sheetName = 'Sheet1'
```


Now we're going to load the file or the workbook using load_workbook() method of openpyxl


```python
workBook = opx.load_workbook(fileName)
```


We all know the structure of a spreadsheet. Data is always stored in sheets. So we need to get the sheet where our data is. Now MS Excel has genereously given us the name Sheet1 so we don't have to cry here and there to get the name. So, houston, let's launch the shuttles and load the sheet!

```python
sheet = workBook.get_sheet_by_name(sheetName)
```


Now we get the row and column count from the workbook. (Let's see if python can load all those records or not! Brute force test ;) )



```python
maxRows = sheet.max_row
print(maxRows)
maxCol = sheet.max_column
print(maxCol)
```

```bash
# output
10001
3
```

 
> **Aw yes! xD**

So it does load all those things. Fascinating! Now to the real part of thing, where we read people's private data( This is where you feel like Google! Although this data is fake. ) and write them to files xD



```python
for i in range(1, maxRows + 1):
    name = sheet.cell(row=i, column=1).value
    outputFile = open('../dump/{}.txt'.format(name), 'w')

    for j in range(1, maxCol + 1):
        outputFile.write(sheet.cell(row=i, column=j).value + '\n')
    outputFile.close()

    # just checking for a count of the write op actually!
    print('Written file number : {}'.format(i))
```

Let's Just add a nice message at the end so people can be assured that we're done!

```python
print('Done writing your business card hooman!')
```


> **Are there actually 10,000 text files written? OMG!**

Why don't we just find it out with another python script?



```python
import os

path = '../dump/'
fileList = os.listdir(path)

fileNo = len(fileList)
print(fileNo)
```

```bash
# output

9382
```



> **Come on! Can't see 10,000 files on my computer! [ Neither can I ]**

Our very friendly Faker generator did some witty stuff and generated some duplicate entries. And that led to the discovery that we're actually looking at 9382 files. Well duplicates will get overwritten easily since we're naming with each person's name after all!

***Attaching a screenshot for ye!***
<img src="http://i.imgur.com/AQS38nq.png" alt="cook-big-excel-py-2" height="600" width="640"/>


> **So where can I find such large excel files?**

Well don't ask me. Better keep your scripts ready when you face those nasty, huge, ugly spreadsheets! Till then I go incognito for chilling out, leaving you to scratch your heads over what just happened. ***Sayonara!***
