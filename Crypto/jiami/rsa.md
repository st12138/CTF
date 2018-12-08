# **RSA** 
- ## 算法 
  1.选择一对不同的、足够大的素数p，q。<br>  2.计算n=pq。<br>
  3.计算f(n)=(p-1)(q-1)，同时对p,q严加保密。<br>
  4.找一个与f(n)互质的数e，且1<e<f(n)。<br>
  5.计算d，使得de≡1modf(n)。<br>
  6.公钥KU=(e,n)，私钥KR=(d,n)。<br>
  7.加密时，先将明文变换成0至n-1的一个整数M。若明文较长，可先分割成适当的组，然后再进       行交换。设密文为C，则加密过程为：C≡M^e(mod n)。<br> 
  8.解密过程为：M≡C^d(mod n)。
--------------------- 
[CSDN] (https://blog.csdn.net/c465869935/article/details/52266867 )

- ## 例子
    1. p=3,q=11  <br>
    2. n=pq=33   <br>
    3. f(n)=20   <br>
    4. e=3       <br>
    5. d=7   ed=21=1 mod(20) <br>
    6. KU=(3,33),KR=(7,33)<br>
    7. 取M=key  k=11 e=5 y=25<br>
    >k C=11^3 mod(33)=11<br>
     e C=5^3  mod(33)=31<br>
     y C=25^3 mod(33)=16<br>

    8.
    >k M=11^7 mod(33)=11<br>
     e M=31^7 mod(33)=5<br>
     y M=16^7 mod(33)=25<br>
