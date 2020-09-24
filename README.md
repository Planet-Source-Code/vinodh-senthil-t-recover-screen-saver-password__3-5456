<div align="center">

## Recover Screen Saver Password


</div>

### Description

Like 2 Recover Your Lost Screen Laver Password using C program ??? To Recover your Lost Screen saver Password with a very little skill in Programming in C, The Programming is only 15 ~ 20 Lines :-)) Enjoy!!!
 
### More Info
 
Only Click Enter

Anyone with a very little knowledge or Skill in C can understand this Coding

U Get what u wanted :-)

No Side Effects


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Vinodh Senthil\.T](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/vinodh-senthil-t.md)
**Level**          |Beginner
**User Rating**    |3.8 (15 globes from 4 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__3-14.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/vinodh-senthil-t-recover-screen-saver-password__3-5456/archive/master.zip)

### API Declarations

Only the C Program


### Source Code

```
#include<stdio.h>
#include<conio.h>
#include<string.h>
#include<ctype.h>
#include<process.h>
void main()
{
  FILE *stream;
  char string[] = "creenSave_Data";
  char msg[16],ch,pass[27];
  int i=1,found=1,j,dec[]={4,8,14,14,7,6,1,13,6,7,6,9,10,1,1,11,7,10,8,12,4,7,15,8,5,4,9,5};
  int pass1[27];
  clrscr();
  printf("--------This program is developed by VINOD SENTHIL.T -------------\n\n\n\n");
  printf("\n\n  Contact ---------> vinod_chan_t@yahoo.com <-----------\n\n\n\n");
  stream = fopen("C:\\WINDOWS\\USER.DAT", "rb");
  if (stream==NULL)
   {
    printf("Cannot open the file");
    getch();
    exit(1);
   }
	while(found)
	{
	 while ((getc(stream))!='S')
	  {};
	   fgets(msg, strlen(string)+1, stream);
	   i=strcmp(string,msg);
	   if (i==0) found=0;
	 }
  while(!found)
   {
   ch=getc(stream);
   if (!(isalpha(ch) || isdigit(ch)))
	 found=1;
   else
	 {
	  pass[i]=ch;
	  i++;
	 }
   }
   for(j=0;j<i;j++)
   {
   if (isalpha(pass[j]))
	  pass1[j]=pass[j]-55;
   else
	  pass1[j]=pass[j]-48;
   pass1[j]=pass1[j]^dec[j];
   }
   printf("     Your Screen Saver Password is : ");
   for (j=0;j<i;j+=2)
	printf("%c",toascii(16*pass1[j]+pass1[j+1]));
  fclose(stream);
  getch();
}
//Please Vote for my Program :-)
```

