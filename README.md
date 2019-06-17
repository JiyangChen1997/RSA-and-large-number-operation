# RSA and large numer operation library write in c/c++


1.rsa3.cpp is the main part, and it relys on bignum3.h<br>

2.The code style and some parts are referenced from the book- Cryptography in C and C++ Second Edition<br>

3.The efficiency is not so good, but if you compile it use the optimization in VS, it seems so good!<br>

4.If you want to test rsa.cpp,you need a file called 'plain.txt' in your project filefolder,and copy the xxxprime.txt to your project folder(or you can do exclu()function at the beginning).You also need to change the 'include' path at the beginning of rsa.cpp. And to avoid errors, the content of plain.txt is suggested to be a SHA-1 result of another file.<br>

5.If you want to test rsa3.cpp,you need a file called 'plain.txt' in your project filefolder.It contained less than 128bytes contents in hex form. It can be SHA-1 result like '4EA72B9F99A196581A8ED410DC3016FC74130B26'. You also need to change the 'include' path at the beginning of rsa3.cpp to include 'bignum3.h'. debug=1 is to find a prime <=1024bits , and debug=0 is to do RSA process. And to avoid errors, the content of plain.txt is suggested to be a SHA-1 result of another file.<br>

6.if you encounter problem below, add _SCL_SECURE_NO_WARNINGS to your C/C++compiler preprocessor definition :
C4996	'std::basic_string<char,std::char_traits<char>,std::allocator<char>>::copy': Call to 'std::basic_string::copy' with parameters that may be unsafe - this call relies on the caller to check that the passed values are correct. To disable this warning, use -D_SCL_SECURE_NO_WARNINGS. See documentation on how to use Visual C++ 'Checked Iterators'	2018tst	d:\密码学\my特别快的rsa and bn\rsa2.cpp	465
  
P.S. 1
rsa3.cpp use the way Knuth provided in his book to implement division. Hence the efficiency enhance rapidly.
-
rsa3.cpp使用了Knuth方法实现了除法，效率大幅提高,随机数用最简单的办法产生，素性检测使用米勒拉宾。
-


P.S. 2
may cause some problem because of it contains Chinese charactars. If so, try to convert the code to UTF-8 or ANSI.
-
因为有中文，会有编码问题，可能需要用notepad++转为UTF-8或者ANSI中的某一种
-

P.S. 3
实现说明
-
1. [总体说明](https://blog.csdn.net/qq_37734256/article/details/84898117)
2. [RSA说明](https://blog.csdn.net/qq_37734256/article/details/84900062)
3. [除法实现](https://blog.csdn.net/qq_37734256/article/details/86751853)
4. [快速求逆](https://blog.csdn.net/qq_37734256/article/details/86776219)
5. [蒙哥马利模幂](https://blog.csdn.net/qq_37734256/article/details/86986291)
6. [素性检验](https://blog.csdn.net/qq_37734256/article/details/87597591)

