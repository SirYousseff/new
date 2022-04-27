int strcmp(char s1[], char s2[])
{
int i = 0;
while (s1[i] != '\0')
{
if ((s2[i] == '\0') || (s1[i] > s2[i]))
return 1;
else if (s1[i] < s2[i])
return -1;
i++;
}
if (s2[i] != '\0')
return -1;
return 0;
}
int strcmp2(char s1[], char s2[])
{
int i;
for(i=0; s1[i] && s2[i];i++)
{
if(s1[i] > s2[i])
return 1;
else if(s1[i] < s2[i])
return -1;
}
if(s1[i] != 0 && s2[i] == 0) return 1;
if(s1[i] == 0 && s2[i] != 0) return -
1;

return 0;
}
Try to write the code for strcmpi(), which is case insensitive

void strcat(char s1[], char s2[])
{
int len1 = strlen(s1);
int i; // we want to use i after the loop
for (i = 0; s2[i]; i++)
s1[len1 + i] = s2[i];
s1[len1 + i] = '\0';
}

int strlen(char s1[])
{
int len = 0;
while(s1[len]) // or for (len = 0; s1[len]; len++);
len++;
return len;
}
We may write the code for toupper:
char toupper(char c)
{
if(c >= 'a' && c <= 'z')
return c - ('a' - 'A'); //ASCII of 'a' is 97 and 'A' is 65
}
