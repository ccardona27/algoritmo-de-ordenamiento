void mergesort(int a[], int l, int r)
{
	int i,j,k,m,b[MAX];
	if (r > l) 
	{
		m = (r+l) /2;
		mergesort(a, l, m);
		mergesort(a, m+1, r);
		for (i= m+1; i > l;i--)
			b[i-1] = a[i-1];
		for (j= m; j < r;j++) 
			b[r+m-j] = a[j+1];
		for (k=l ; k <=r; k++)
			if(b[i] < b[j])
			   a[k] = b[i++];
			else
			   a[k] = b[j--];
	}
}

a = {a,s,o,r,t,i,n,g,e,x,a,m,p,l,e}
      {a,s,
            o,r,
       a,o,r,s,
                 i,t,
                     g,n,
                 g,i,n,t,
       a,g,i,n,o,r,s,t,
                          e,x,
                               a,m,
                          a,e,m,x,
                                     l,p,
                                     e,l,p}
                          a,e,e,l,m,p,x}
