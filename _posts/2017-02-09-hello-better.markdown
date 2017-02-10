---
layout:     post
title:      "Hello 2017"
subtitle:   " Hello World, Hello Blog"
date:        2017-02-09 19:13:00
author:     "Luoyayu"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 生活
---

> “Yeah It's on. ”

#### 正文
youtube播放器测试：
{% youtube sD0NjbwqlYw %}

Jekyll 主题 fork 了 *Clean Blog*，标签支持来自*Hux* 支持

今后会添加web slider #iframe

Theme 的 CSS 是基于 Bootstrap 定制的，

中文字体的渲染，fork 了 [Type is Beautiful](http://www.typeisbeautiful.com/) 的 `font` CSS，调整了字号，适配了 Win 的渣渲染。

C++代码测试：

{% highlight cpp %}
struct matrix
{
    int a[15][15];
};
matrix mat1;
matrix mat2;
matrix function(matrix mat1,matrix mat2,int mod)
{
    int i,j,k;
    matrix T;
    memset(T.a,0,sizeof T.a);
    for(i=0;i<2;i++)
    {
        for(j=0;j<2;j++)
        {
            for(k=0;k<2;k++)
            {
                T.a[i][j]=(T.a[i][j]+mat1.a[i][k]*mat2.a[k][j]%mod)%mod;
            }
        }
    }
    return T;
    memset(T.a,0,sizeof T.a);
}
int main()
{
      int A,B;
    __int64 n;
    __int64 mod=7;
      while(scanf("%d%d%I64d",&A,&B,&n)==3)
      {
          if(A==0&&B==0&&n==0)break;
          mat1.a[0][0]=A;mat2.a[0][0]=A;
          mat1.a[0][1]=B;mat2.a[0][1]=B;
          mat1.a[1][0]=1;mat2.a[1][0]=1;
          mat1.a[1][1]=0;mat2.a[1][1]=0;
          if(n==1||n==2)
          {
              printf("1\n");
          }
          else
          {
              n=n-3;
              while(n!=0)
              {
                  if(n&1)
                  mat1=function(mat1,mat2,mod);
                  mat2=function(mat2,mat2,mod);
                  n>>=1;
              }
              printf("%d\n",(mat1.a[0][0]+mat1.a[0][1])%mod);
          }
      }
return 0;
}

{% endhighlight %}


