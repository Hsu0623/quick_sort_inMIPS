# quick_sort_inMIPS
using MIPS to write quick sort
### in C ####
void qsort(int a[], int lo, int hi)
{
	int i = lo, j = hi, h;
	int x = a[(lo + hi) / 2];
	do
	{
		while (a[i] < x) i++;
		while (a[j] > x) j--;
		if (i <= j) 
		{
			h = a[i];
			a[i] = a[j]; 
			a[j] = h;
			i++;
			j--;
        }
	}while (i <= j)
	if (lo < i) qsort(a, lo, j);
	if (i < hi) qsort(a, i, hi);
}
