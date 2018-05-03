
void quicksort(int a[], int l, int r)
{
	int i,j,v;
	if(r > l)
	{
		v = a[r];
		i = l-1;
		j = r;
		for(;;)
		{
			while(a[++i] < v && i < r);
			while(a[--j] > v && j > l);
			if( i >= j)
				break;
			swap(a,i,j);			
		}
		swap(a,i,r);
		quicksort(a,l,i-1);
		quicksort(a,i+1,r);
	}
}
