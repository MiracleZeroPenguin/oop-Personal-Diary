# README

## Requirements

The Personal Diary is a CLI (Command Line Interface) software, consists of four programs:

```
pdadd 
pdlist [ ]
pdshow 
pdremove 
```

- **`pdadd`** is used to add an entity to the diary for the date. If an entity of the same date is in the diary, the existing one will be replaced. pdadd reads lines of the diary from the stdin, line by line, until a line with a single `'.'` character or the `EOF` character (`Ctrl-D` in Unix and `Ctrl-Z` in Windows).
- **`pdlist`** lists all entities in the diary ordered by date. If the `start` and the `end` date are provided through command line parameters, it lists entities between the start and the end only. This program lists to the stdout.
- **`pdshow`** prints the content of the entity specified by the date to the stdout.
- **`pdremove`** removes one entity of the date. It returns 0 on success and -1 on failure.

The software stores the diary in one data file, and reads it to the memory at the beginning of each program, and stores it back to the file at the end of the process.

## Evaluation standard

1. c++ code quality (clean, compact and reasonable)
2. comments quality
3. common classes and functions should be shared between programs
4. these programs are physically independent so direct interaction is not permitted
5. these programs are able to work together by means of redirection
6. these programs are able to be used in a shell/batch script

## 程序说明

1. exe文件夹中为包含四个程序的可执行文件
2. include文件夹中为diary相关文件头与函数定义
3. src文件夹中为四个独立的主函数包括
   	pdadd.c		|	添加日记或重置当日日记
   pdlist.c	     |	列出所有日记或规定时间区间内日记
   pdshow.c	   |	展示指定日期日记
   pdremove.c	|	删除指定日期日记
4. 编译环境为visual studio 2019

## CopyRight

* FileName:		Personal Diary
* Author:		Miracle_Zero
* Date:		2020/4/25
  

