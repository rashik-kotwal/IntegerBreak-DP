# IntegerBreak-DP

For the Recursive implementation, Time limit exceeded, but answers were coming correct till ~n=40

int integerBreak(int n)
{
if(n<=2)
    return 1;
 
int max_val=Integer.MIN_VAL;
for(int i=2;i<=n;i++)
{
      max_val=max(max_val,i*integerBreak(n-i));
}

return max_val;
}

Again, for n=3, answer was coming incorrect (3, but it should be 2)

Handled this case separately for the DP solution, and all testcases passed
