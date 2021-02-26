#include <iostream>
using namespace std;

void f1_1(int n)
{
	int arr[11] = {};
	arr[0] = 1;
	for (int i = 1; i < n; i++)
	{
		arr[i] = arr[i - 1] + 2;
		cout << arr[i] << endl;
	}
}

void f1_2(int n)
{
	int arr[11]{};

	for (int i = 0, a = 1; i < n; i++, a += 2)
	{
		arr[i] = a;
		cout << arr[i] << endl;
	}
}

void f2(int n)
{
	int arr[11]{};
	arr[0] = 1;
	for (int i = 0, a = 1; i < n; i++, a *= 2)
	{
		arr[i] = a;
		cout << arr[i] << endl;
	}
}

void f3(int a, int d, int n)
{
	int arr[11]{};
	arr[0] = 1;
	for (int i = 0; i < n; i++) 
	{
		arr[i] = a + (d * i);
		cout << arr[i] << endl;
	}
}

void f4(int a, int d, int n)
{
	int arr[11]{};
	for (int i = 0; i < n; i++)
	{
		arr[i] = a + pow(d,i);
		if (i ==0)
		{
			arr[0] -= 1;
		}
		cout << arr[i] << endl;
	}
}

void f5(int n)
{
	int arr[11]{};
	arr[0] = 1;
	arr[1] = 1;
	for (int i = 2; i < n; i++)
	{
		arr[i] = arr[i - 1] + arr[i-2];
		cout << arr[i] << endl;
	}
}

void f6(int a, int b, int n)
{
	int arr[11]{};
	arr[0] = a;
	arr[1] = b;
	int sum = 0;
	for (int i = 0; i < n; i++)
	{
		
		if (i > 1)
		{
			arr[i] = sum;
		}
		sum += arr[i];
		cout << arr[i] << endl;
	}
}

void f7(int n)
{
	int arr[11]{};
	arr[10] = 11;
	for (int i = n; i > 0; --i)
	{
		arr[i] = i;
		cout<<arr[i]<<endl;
	}
}

void f8(int n)
{
	int count = 0;
	int arr[11]{};
	for (int i = 0; i <= n; i++)
	{
		arr[i] = i;
		if (arr[i]%2!=0)
		{
			count += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count;
}

void f9(int n)
{
	int count = 0;
	int arr[11]{};
	for (int i = n; i > 0; i--)
	{
		arr[i] = i;
		if (arr[i] % 2 == 0)
		{
			count += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count;
}

void f10(int n)
{
	int count1 = 0;
	int count2 = 0;
	int arr[11]{};
	for (int i = 0; i <= n; i++)
	{
		arr[i] = i;
		if (arr[i] % 2 == 0)
		{
			count1 += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count1 << endl;
	for (int i = n; i > 0; i--)
	{
		arr[i] = i;
		if (arr[i] % 2 != 0)
		{
			count2 += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count2;
}

void f11(int n,int k)
{
	int arr[11] {1,5,8,7,9,6,8,7,3,6,5};
	for (int i = 0; i <= n; i++)
	{	 
		if (arr[i] % k == 0)
		{
			cout << arr[i]<<endl;
		}

	}
}

void f12(int n)
{ 
	int arr[11]{};
	for (int i = 0; i < n; i++)
	{ 
		if (i % 2 == 0)
		{
			cout << i << endl;
		}
	}
}

void f13(int* arr,int n )
{
	
	for (int i = 0; i < n; i++)
	{
		if (i % 3 == 0)
		{
			arr[i] = i;
			cout << i << endl;
		}
	}
}

void f14(int* arr, int n)
{

	for (int i = 0; i < n; i++)
	{
		if (i % 2 != 0)
		{
			arr[i] = i;
			cout << i << endl;
		}
	}
	for (int i = 0; i < n; i++)
	{
		if (i % 2 == 0)
		{
			arr[i] = i;
			cout << i << endl;
		}
	}
}

void f15(int* arr, int n)
{
	int i = 0;
	for (int i = 0; i < n; i++)
	{
		if (i % 2 != 0)
		{
			cout << i << endl;
		}
	}
	for (n; n != 0; n--)
	{
		if (n % 2 == 0)
		{
			cout << n << endl;
		}
	}
}

void d(int size, int* arr)
{
	for (int i = 0; i < size; i++)
	{
		arr[i] = i;
	}
	for (int i = 0; i < size; i++)
	{
		if (arr[i] % 2 == 5)
		{
			cout << arr[i];
		}
	}
}

void f16(int n)
{
	int arr[11]{};
	for (int i = 1; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
		
	}
	cout << endl;
	for (int i = 1; i < n / 2; ++i)
	{
		cout << arr[i];
		cout << arr[n - 1 - i];
	}
}

void f17(int n)
{
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	cout << endl;
	for (int i = 0; i < n / 2 + 1; i += 2)
	{
		cout << arr[i] << endl;
		if (i < n / 2)
		{
			cout << arr[i + 1] << endl;
		}
		if (n - i - 1 > n / 2)
		{
			cout << arr[n - i - 1] << endl;
		}
		if (n - i - 2 > n / 2)
		{
			cout << arr[n - i - 2] << endl;
		}
	}
}

void f18(int n)
{
	int arr[11]{};
	//for (int i = 1; i < n; ++i)//для авто-ввода переменных
	//{
	//	arr[i] = i;
	//	cout << arr[i] << endl;
	//}
	//for (int i = 0; i < n; i++)//для ручного ввода переменных
	//{
	//	cin >> arr[i];
	//	cout << arr[i];
	//}
	cout << endl;
	for (int i = 0; i < 10; ++i)
	{
		cout << arr[i + 1] << endl;
		for (int i = 0; arr[i] >= arr[9]; ++i)
		{
			if (i == 10)
			{
				cout << '0';
			}
			cout << arr[i];
		}
	}
	
}

void f19(int n)
{
	int i;
	int arr[11]{};
	for (int i = 1; i < 11; i++)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	i = 9;
	cout << endl;
	while (((arr[0] >= arr[i]) || (arr[i] >= arr[10])) && (i > 0))
	{
		--i;
	}
	if (i == 0)
	{
		cout << i;
	}
	cout << arr[i];
}

void f20(int n, int k, int l)
{
	int arr[11]{};
	for (int i = 1; i < n; i++)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int sum = 0;
	cout << endl;
	for (int i = k - 1; i <= l - 1; ++i)
	{
		sum += arr[i];
	}
	cout << sum;
}

void f21(int n, int b, int c)
{
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	double sum = 0;
	for (int i = b - 1; i <= c - 1; ++i)
	{
		sum += arr[i];
	}
	cout << sum / (c - b + 1);
}

void f22(int n, int k, int l)
{
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	} 
	int sum = 0;
	for (int i = 0; i < k - 1; ++i)
	{
		sum += arr[i];
	 }
	for (int i = l; i < n; ++i)
	{
		sum += arr[i];
	}
	cout << sum;
}

void f23(int n,int k,int l)
{
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	double sum = 0;
	for (int i = 0; i < k - 1; ++i)
	{
		sum += arr[i];
	}
	for (int i = l; i < n; ++i)
	{
		sum += arr[i];
	}
	cout << sum / (k - 1 + (n - l));
}

void f24(int n)
{
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int r = arr[1] - arr[0];
	for (int i = 1; i < n; ++i)
	{
		if (r != arr[i] - arr[i - 1])
		{
			r = 0;
		}
	}
	cout << r;
}

void f25(int n)
{
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	double z = arr[1] / arr[0];
	for (int i = 1; i < n; ++i)
	{
		if (z != arr[i] / arr[i - 1])
		{
			z = 0;
		}
	}
	cout << z;
}

void f26(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int temp = arr[0] % 2;
	for (int i = 1; ((i < n) && (temp != arr[i] % 2)); ++i)
	{
		temp = arr[i] % 2;
	}
	if (i == n)
	{
		cout << 0;
	}
	else
	{
		cout << i + 1;
	}
	
}

void f27(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int temp = arr[0]>1;
	for (int i = 1; ((i < n) && (temp != arr[i] % 2)); ++i)
	{
		temp = arr[i]>1;
	}
	if (i == n)
	{
		cout << 0;
	}
	else
	{
		cout << i + 1;
	}

}

void f28(int n)
{
	int min = INT_MAX;//максимальное значение типа инт,для всех случаев,если инициализация массива будет ручная
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	cout << endl;
	for (int i = 0; i < n; i++)
	{
		if (i % 2 == 0)
		{
			if (arr[i] < min)
			{
				min = arr[i];
			}
		}
	}
	cout << min;
}

void f29(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int max = arr[0];
	for (i = 0; i < n; i += 2)
	{
		if (arr[i] > max)
		{
			max = arr[i];
		}
	}
	cout << endl;
	cout << max;
}

void f30(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int num = 0;
	for (i = 0; i < n - 1; ++i)
	{
		if (arr[i] > arr[i + 1])
		{
			++num;
		}
	}
	cout << endl;
	cout << num;
}

void f31(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int num = 0;
	for (i = n - 1; i >= 1; --i)
	{
		if (arr[i - 1] < arr[i]) 
		{
			++num;
		}
	}
	cout << endl;
	cout<< num;
}

void f32(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	if (arr[0] < arr[1])
	{
		cout << 1;
	}
	else
	{
		i = 1;
		while ((i < n - 1) && !((arr[i - 1] > arr[i]) && (arr[i] < arr[i + 1]))) 
		{
			++i;
		}
		cout << i + 1;
	}
}

void f33(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	if (arr[n - 1] > arr[n - 2]) 
	{
		cout<<n;
	}
	else 
	{
		i = n - 2;
		while ((i >= 1) && !((arr[i - 1] < arr[i]) && (arr[i] > arr[i + 1]))) 
		{
			--i;
		}
		cout << i + 1;
	}
}

void f34(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int c = 1;
	int max;

	for (i = 1; i < n - 1; ++i) 
	{
		if ((arr[i - 1] > arr[i]) && (arr[i] < arr[i + 1]))
		{
			if ((arr[i] > max) || c) 
			{
				max = arr[i];
				c = 0;
			}
		}
	}
	if ((arr[0] < arr[1]) && ((arr[0] > max) || c)) {
		max = arr[0];
		c = 0;
	}
	if ((arr[n - 1] < arr[n - 2]) && ((arr[n - 1] > max) || c)) {
		max = arr[n - 1];
		c = 0;
	}

	cout << max;
}

void f35(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int c = 1;
	int min;

	for (i = 1; i < n - 1; ++i) 
	{
		if ((arr[i - 1] < arr[i]) && (arr[i] > arr[i + 1]))
		{
			if ((arr[i] < min) || c)
			{ 
				min = arr[i];               
				c = 0;
			}
		}
	}   
	if ((arr[0] > arr[1]) && ((arr[0] < min) || c)) 
	{
		min = arr[0];     
		c = 0; 
	}     
	if ((arr[n - 1] > arr[n - 2]) && ((arr[n - 1] < min) || c)) 
	{
		min = arr[n - 1];
		c = 0;
	}

	cout << min;
}

void f36(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int c = 1, max = 0;
	for (i = 1; i < n - 1; ++i) 
	{
		if (!((arr[i - 1] < arr[i]) && (arr[i] > arr[i + 1])) && !((arr[i - 1] > arr[i]) && (arr[i] < arr[i + 1])))
		{
			if ((arr[i] > max) || c)
			{
				max = arr[i];
				c = 0;
			}
		}
	}
	if ((arr[0] == arr[1]) && ((arr[0] > max) || c)) 
	{
		max = arr[0];
		c = 0;
	}
	if ((arr[n - 1] == arr[n - 2]) && ((arr[n - 1] > max) || c)) 
	{
		max = arr[n - 1];
		c = 0;
	}

	cout << max;
}

void f37(int n)
{
	int i;
	int num = 0;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = 2; i < n; ++i)
	{
		if ((arr[i - 2] < arr[i - 1]) && !(arr[i - 1] < arr[i])) 
		{
			++num;
		}

	}
	if (arr[n - 2] < arr[n - 1])
	{
		++num;
	}
	cout << num;
}

void f38(int n)
{
	int i;
	int num = 0;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = 2; i < n; ++i)
	{
		if ((arr[i - 2] < arr[i - 1]) && !(arr[i - 1] < arr[i]))
		{
			++num;
		}
	}
	if (arr[n - 2] < arr[n - 1])
	{
		++num;
	}
	cout << num;
}

void f39(int n)
{
	int i;
	int num = 0;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
    for (i=2;i<n;++i)
	{
        if ((arr[i-2]>arr[i-1]) && !(arr[i-1]>arr[i]))
		{
            ++num;
        }
        if ((arr[i-2]<arr[i-1]) && !(arr[i-1]<arr[i]))
		{
            ++num;
        }
    }
 
	if (arr[n - 2] != arr[n - 1])
	{
		++num;
	}
	cout << num;
}

void f40(int n,int r)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int min = abs(arr[0] - r), k = 1;

	for (i = 1; i < n; ++i) 
	{
		if ((abs(arr[i] - r)) < min)
		{
			min = (abs(arr[i] - r));
			k = i;
		}
	}
	cout << arr[k];
}

void f41(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int summax = arr[0] + arr[1], k = 1;

	for (i = 2; i < n; ++i)
	{
		if ((arr[i - 1] + arr[i]) > summax)
		{
			summax = arr[i - 1] + arr[i];
			k = i;
		}
	}
	cout<< arr[k - 1]<<arr[k];
}

void f42(int n,int r)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int min = abs(arr[0] + arr[1] - r), k = 1;

	for (i = 2; i < n; ++i)
	{
		if (abs(arr[i - 1] + arr[i] - r) < min)
		{
			min = abs(arr[i - 1] + arr[i] - r);
			k = i;
		}
	}
	cout<< arr[k - 1]<<arr[k];
}

void f43(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int num = 1;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i]) 
		{
			++num;
		}
	}
	cout<< num;
}

void f44(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2;
	for (i = 0; i < n - 1; ++i)
	{
		for (i2 = i + 1; i2 < n; ++i2)
		{
			if (arr[i] == arr[i2])
			{
				cout<< i + 1<<endl<< i2 + 1;
			}
		}
	}
}

void f45(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2, k = 0, k2 = 1;
	for (i = 0; i < n - 1; ++i) 
	{
		for (i2 = i + 1; i2 < n; ++i2)
		{
			if (abs(arr[i] - arr[i2]) < abs(arr[k] - arr[k2]))
			{
				k = i;
				k2 = i2;
			}
		}
	}
	cout<< k + 1<<endl<< k2 + 1;
}

void f46(int n,int r)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2, k = 0, k2 = 1;
	for (i = 0; i < n - 1; ++i) 
	{
		for (i2 = i + 1; i2 < n; ++i2) 
		{
			if (abs(arr[i] + arr[i2] - r) < abs(arr[k] + arr[k2] - r))
			{
				k = i;
				k2 = i2;
			}
		}
	}
	cout<< k + 1<<endl<< k2 + 1;
}

void f47(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2, num = 1;
	for (i = 1; i < n; ++i, ++num)
	{
		for (i2 = i - 1; i2 >= 0; --i2)
		{
			if (arr[i] == arr[i2])
			{
				--num;
			}
		}
	}
	cout << num;
}

void f48(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2, nummax = 0;
	for (i = 0; i < n; ++i)
	{
		int num = 1;
		for (i2 = i + 1; i2 < n; ++i2)
		{
			if (arr[i] == arr[i2])
			{
				++num;
			}
		}
		if (num > nummax) 
		{
			nummax = num;
		}

	}
	cout<< nummax;
}

void f49(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2;
	for (i = 1; i <= n; ++i)
	{
		for (i2 = 0; i2 < n; ++i2) 
		{
			if (arr[i2] == i)
			{
				i2 = n + 100;
				break;
			}

		}
		if (i2 != n + 100)
		{
			cout << i;
			break;
		}

	}
	if (i == n + 1) 
	{
		cout << 0;
	}
}

void f50(int n)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int num = 0, i2;
	for (i = 0; i < n - 1; ++i) 
	{
		for (i2 = i + 1; i2 < n; ++i2) 
		{
			if (arr[i] > arr[i2])
			{
				num++;
			}
		}
	}
	cout<<num;
}

void f51(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)//Массив А
	{
		arr[a] = a;//
		cout << arr[i] << endl;
	}
	for (int b = 0; b < n; ++b)//Массив В
	{
		arr[b] = b;//
		cout << arr[i] << endl;
	}
	for (i = 0; i < n; ++i)
	{
		arr[a] += arr[b];
		arr[b] = arr[a] - arr[b];
		arr[a] = arr[a] - arr[b];
	}
	cout << "MaccuB A:" << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[a];
	}
	cout << "MaccuB B:" << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[b];
	}
}

void f52(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (i = 0; i < n; ++i)
	{
		if (arr[a] < 5)
		{
			arr[b] = 2 * arr[a];
		}
		else
		{
			arr[b] = arr[a] / 2;
		}
	}
	cout<<" MaccuB B : " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[b];
	}
}

void f53(int n)
{
	int i;
	int a, b, c;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int b = 0; b < n; ++b)
	{
		arr[b] = b;
		cout << arr[b] << endl;
	}
	for (c = 0; c < n; ++c) 
	{
		if (arr[a] > arr[b]) 
		{
			arr[c] = arr[b];
		}
			
		else 
		{
			arr[c] = arr[b];
		}
			
	}
	cout << " MaccuB C : " << endl;
	for (i = 0; i < n; ++i) 
	{
		cout << arr[c];
	}
		
}

void f54(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i = 0;
	for (i = 0; i < n; ++i) 
	{
		if (arr[a] % 2 == 0)
		{
			arr[b] = arr[a];
			b++;
		}
	}

	cout<<" size: "<<b;

	for (i = 0; i< b; ++i)
	{
		cout << arr[b];
	}
		
}

void f55(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a< n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c = -1;
	for (i = 0; i < n; i += 2)
	{
		++c;
		arr[b] = arr[a];
	}

	cout<<" B: "<< "size: "<<++i;
	for (i = 0; i < c; ++i) 
	{
		cout << arr[b];
	}
}

void f56(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] =a;
		cout << arr[a] << endl;
	}
	int c = 0;
	for ( i= 2; i< n; i += 3)
	{
		arr[b] = arr[a];
		++c;
	}

	cout<<"B:" <<" size: "<<i;
	for (i= 0; i < c; ++i) 
	{
		cout << arr[b];
	}
}

void f57(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	int c = 0;
	for (i = 0; i < n; i += 2)
	{
		arr[b] = arr[a];
		++c;
	}

	for (i = 1; i < n; i += 2)
	{

		arr[b] = arr[a];
		++c;
	}

	cout << "B:" << endl;
	for (i = 0; i < c; ++i)
	{
		cout << arr[b];
	}
}

void f58(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c;
	for (i = 0; i < n; ++i)
	{
		arr[b] = 0;
		for (c = 0; c <= i; ++c)
		{
			arr[b] += arr[a];
		}
	}

	cout << "B:" << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[b];
	}
}

void f59(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c;
	for (i = 0; i < n; ++i)
	{
		arr[b] = 0;
		for (c= 0; c <= i; ++c)
		{
			arr[b] += arr[a];
		}
		arr[b] /= i + 1;
	}
	cout << "B:" << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[b];
	}
}

void f60(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c;
	for (i = 0; i < n; ++i) 
	{
		arr[b] = 0;
		for (c = i; c < n; ++c)
		{
			arr[b] += arr[a];
		}
	}
	cout << "B:" << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[b];
	}
}

void f61(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c;
	for (i = 0; i < n; ++i)
	{
		arr[b] = 0;
		for (c = i; c < n; ++c)
		{
			arr[b] += arr[a];
		}
		arr[b] /= (n - i);
	}

	cout << "B: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout<<arr[b];
	}
}

void f62(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c = 0;
	for (i = 0; i < n; ++i) 
	{
		if (arr[a] > 0)
		{
			arr[b] = arr[a];
			++b;
		}
		if (arr[a] < 0) 
		{
			arr[c] = arr[a];
			++c;
		}

	}

	cout<<"B: "<<endl;
	for (i = 0; i< b; ++i)
	{
		cout<< arr[b];
	}
	cout << "C: " << endl;
	for (i = 0; i < c; ++i)
	{
		cout<< arr[c];
	}
}

void f63(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int c;
	for (i= 0; i < 10; ++i) 
	{
		if ((a >= 5) || ((arr[a] > arr[b]) && (b < 5)))
		{
			arr[c] = arr[b];
			++b;
		}
		else
		{
			arr[c] = arr[a];
			++a;
		}
	}
	cout << "C: " << endl;
	for (i = 0; i < 10; ++i) 
	{
		cout<< arr[c];
	}
}

void f64(int n)
{
	int i;
	int a, b,c,d;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	d = a + b + c;
	int ia = 0, ib = 0, ic = 0;
	for (i = 0; i < d; ++i)
	{
		if ((ia < a) && ((ib >= b) || (arr[ia] >= arr[ib])) && ((ic >= c) || (arr[ia] > arr[ic])))
		{
			arr[d] = arr[ia];
			++a;
		}
		else if ((ib < b) && ((ic >= c) || (arr[ib] > arr[ic])))
		{
			arr[d] = arr[ib];
			++b;
		}
		else
		{
			arr[d] = arr[ic];
			++c;
		}
	}
	cout << "D: " << endl;
	for (i = 0; i < d; ++i)
	{
		cout << arr[d];
	}
}

void f65(int n)
{
	int i;
	int a, b, c, d;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int ai = arr[a - 1];

	for (i = 0; i < n; ++i)
	{
		arr[a] += ai;
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[a];
	}
}

void f66(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int even = 0;

	for (a = 0; a < n; ++a)
	{
		if (arr[a] % 2 == 0)
		{
			even = arr[a];
			break;
		}
	}

	for (a = 0; a < n; ++a)
	{
		if (arr[a] % 2 == 0)
		{
			arr[a] += even;
		}
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i) 
	{
		cout << arr[a];
	}
}

void f67(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int odd = 0;

	for (i = n - 1; i >= 0; --i) 
	{
		if (arr[i] % 2 != 0) 
		{
			odd = arr[i];
			break;
		}
	}

	for (; i >= 0; --i)
	{
		if (arr[i] % 2 != 0)
		{
			arr[i] += odd;
		}
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i) 
	{
		cout << arr[i];
	}
}

void f68(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i< n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int min = 0, max = 0;

	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] > arr[max])
		{
			max = i;
		}
		if (arr[i] < arr[min])
		{
			min = i;
		}
	}

	if (max != min) 
	{
		arr[max] += arr[min];
		arr[min] = arr[max] - arr[min];
		arr[max] = arr[max] - arr[min];
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i) 
	{
		cout << arr[i];
	}
}

void f69(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = 1; i < n; i += 2)
	{
		arr[i] += arr[i - 1];
		arr[i - 1] = arr[i] - arr[i - 1];
		arr[i] = arr[i] - arr[i - 1];
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f70(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = 0; i < n / 2; ++i)
	{
		arr[i] += arr[n / 2 + i];
		arr[n / 2 + i] = arr[i] - arr[n / 2 + i];
		arr[i] = arr[i] - arr[n / 2 + i];
	}

	cout << "A: " <<endl ;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f71(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = 0; i < n / 2; ++i)
	{
		arr[i] += arr[n - i - 1];
		arr[n - i - 1] = arr[i] - arr[n - i - 1];
		arr[i] = arr[i] - arr[n - i - 1];
	}

	cout << "A: ";
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f72(int n, int k, int l)
{
	int i;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = k - 1; i < k + (l - k) / 2; ++i)
	{
		//i <> (l-1)-i+(k-1)
		if (i != (l - i + k - 2))
		{
			arr[i] += arr[l - i + k - 2];
			arr[l - i + k - 2] = arr[i] - arr[l - i + k - 2];
			arr[i] = arr[i] - arr[l - i + k - 2];
		}
	}

	cout << "A: ";
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f73(int n, int k, int l)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = k; i < k + (l - k) / 2; ++i)
	{
		//i <> (l-1)-i+(k-1)
		//printf("%i, %i \n",i,l-i+k-2);
		if (i != (l - i + k - 2))
		{
			arr[i] += arr[l - i + k - 2];
			arr[l - i + k - 2] = arr[i] - arr[l - i + k - 2];
			arr[i] = arr[i] - arr[l - i + k - 2];
		}
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f74(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int min = 0, max = 0;

	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] > arr[max])
		{
			max = i;
		}
		if (arr[i] < arr[min])
		{
			min = i;
		}
	}

	if (max < min)
	{
		max += min;
		min = max - min;
		max = max - min;
	}

	for (i = min + 1; i < min + (max - min); ++i)
	{
		arr[i] = 0;
	}
	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f75(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int min = 0, max = 0;

	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] > arr[max]) max = i;
		if (arr[i] < arr[min]) min = i;
	}

	if (max < min)
	{
		max += min;
		min = max - min;
		max = max - min;
	}

	for (i = min; i < min + 1 + (max - min) / 2; ++i)
	{
		if (i != (max - i + min))
		{
			arr[i] += arr[max - i + min];
			arr[max - i + min] = arr[i] - arr[max - i + min];
			arr[i] = arr[i] - arr[max - i + min];
		}
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f76(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	if (arr[0] > arr[1])
	{
		i = 2;
		arr[0] = 0;
	}
	else i = 1;

	for (; i < n - 1; ++i)
	{
		if ((arr[i - 1] < arr[i]) && (arr[i] > arr[i + 1]))
		{
			arr[i] = 0;
			++i;
		}
	}

	if ((i == n - 1) && (arr[n - 2] < arr[n - 1]))
	{
		arr[n - 1] = 0;
	}
	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f77(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	if (arr[0] < arr[1]) 
	{
		i = 2;
		arr[0] *= arr[0];
	}
	else i = 1;

	for (; i < n - 1; ++i) 
	{
		if ((arr[i - 1] > arr[i]) && (arr[i] < arr[i + 1]))
		{
			arr[i] *= arr[i];
			++i;
		}
	}

	if ((i == n - 1) && (arr[n - 2] > arr[n - 1]))
	{
		arr[n - 1] *= arr[n - 1];
	}
	cout<<"A: "<<endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f78(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	double ai1, ai = arr[0];
	arr[0] = (ai + arr[1]) / 2;
	for (i = 1; i < n - 1; ++i)
	{
		ai1 = ai;
		ai = arr[i];
		arr[i] = (ai1 + ai + arr[i + 1]) / 3;
	}

	arr[n - 1] = (arr[n - 1] + ai) / 2;

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f79(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = n - 1; i >= 1; --i)
	{
		arr[i] = arr[i - 1];
	}
	arr[0] = 0;

	cout<<"A: ";
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f80(int n)
{
	int i;
	int a, b;
	int arr[11]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	for (i = 0; i < n - 1; ++i)
	{
		arr[i] = arr[i + 1];
	}
	arr[n - 1] = 0;

	cout<<"A: "<<endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f120(int n)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2;
	for (i = 0; i < n; ++i)
	{
		if (i + 1 < n)
		{
			if (arr[i] != arr[i + 1])
			{
				--n;
				for (i2 = i; i2 < n; ++i2) arr[i2] = arr[i2 + 1];
				{
					--i;
				}
			}
		}
	}
	--n;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f121(int n, int k)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int num = 1;
	for (i = 0; (i < n - 1) && (num < k); ++i)
	{
		if (arr[i] != arr[i + 1])
		{
			++num;
		}
	}
	int begine = i;

	for (i = begine; (i < n - 1); ++i)
	{
		if (arr[i] != arr[i + 1])
		{
			break;
		}
	}
	int ende = i;
	int i2;
	for (i2 = 1; i2 <= ende - begine + 1; ++i2)
	{
		n++;
		for (i = n - 1; i > ende; i--)
		{
			arr[i] = arr[i - 1];
		}
	}
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f122(int n, int k)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int nk = 1, lenserial = (k == 1 ? 1 : 0);

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			nk++;
		}
		if (nk == k)
		{
			lenserial++;
		}
		if (nk > k)
		{
			arr[i - lenserial] = arr[i];
		}
	}
	n -= lenserial;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f123(int n, int k)
{
	int i;
	int a, b;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[a] << endl;
	}
	int i2 = -1, len1series = 1, lenkseries = 0, endkseries, nk = 1;

	for (i = 0; i < 20; ++i)
	{
		arr[i2] = 0;
	}
	for (i = 1; (i < n) && (nk <= k); ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			nk++;
		}
		if (nk == 1)
		{
			len1series++;
		}
		if (nk == k)
		{
			lenkseries++;
			arr[++i2] = arr[i];
		}
		endkseries = i;
	}

	for (i = len1series, nk = 1; (i < n) && (i < endkseries - lenkseries); ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			nk++;
		}
		arr[++i2] = arr[i];
	}

	for (i = 0; i < len1series; ++i)
	{
		arr[++i2] = arr[i];
	}
	for (i = endkseries; i < n; ++i)
	{
		arr[++i2] = arr[i];
	}
	for (i = 0; i < n; ++i)
	{
		arr[i] = arr[i2];
	}
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f124(int n)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int nk = 1, beginkseries = 1, lenkseries = (n == 1 ? 1 : 0), beginendseries;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			nk++;
			if (nk == n)
			{
				beginkseries = i;
			}
			beginendseries = i;
		}
		if (nk == n)
		{
			lenkseries++;
		}
	}

	int i2 = -1;
	for (i = 0; i < beginkseries; ++i)
	{
		arr[++i2] = arr[i];
	}
	for (i = beginendseries; i < n; ++i)
	{
		arr[++i2] = arr[i];
	}
	for (i = beginkseries + lenkseries; i < beginendseries; ++i)
	{
		arr[++i2] = arr[i];
	}
	for (i = beginkseries; i < beginkseries + lenkseries; ++i)
	{
		arr[++i2] = arr[i];
	}
	for (i = 0; i < n; ++i)
	{
		arr[i] = arr[i2];
	}
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f125(int n, int l)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2 = -1, len = 1, i3, endn = n;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len < l)
			{
				arr[++i2] = 0;
				endn -= len - 1;
			}
			else
			{
				for (i3 = 0; i3 < len; ++i3)
				{
					arr[++i2] = arr[i - 1];
				}
			}
			len = 0;
		}
		++len;
	}

	if (len < l)
	{
		arr[++i2] = 0;
		endn -= len - 1;
	}
	else
	{
		for (i3 = 1; i3 <= len; ++i3)
		{
			arr[++i2] = arr[i - 1];
		}
	}

	for (i = 0; i < endn; ++i)
	{
		arr[i] = arr[i2];
	}
	for (i = 0; i < endn; ++i)
	{
		cout << arr[i];
	}
}

void f126(int n, int l)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2 = -1, len = 1, i3, endn = n;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len == l)
			{
				arr[++i2] = 0;
				endn -= len - 1;
			}
			else
			{
				for (i3 = 0; i3 < len; ++i3)
				{
					arr[++i2] = arr[i - 1];
				}
			}
			len = 0;
		}
		++len;
	}

	if (len == l)
	{
		arr[++i2] = 0;
		endn -= len - 1;
	}
	else
	{
		for (i3 = 0; i3 < len; ++i3)
		{
			arr[++i2] = arr[i - 1];
		}
	}

	for (i = 0; i < endn; ++i)
	{
		arr[i] = arr[i2];
	}
	for (i = 0; i < endn; ++i)
	{
		cout << arr[i];
	}
}

void f127(int n, int l)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int i2 = -1, len = 1, i3, endn = n;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len > l)
			{
				arr[++i2] = 0;
				endn -= len - 1;
			}
			else
			{
				for (i3 = 0; i3 < len; ++i3)
				{
					arr[++i2] = arr[i - 1];
				}
			}
			len = 0;
		}
		++len;
	}
	if (len > l)
	{
		arr[++i2] = 0;
		endn -= len - 1;
	}
	else
	{
		for (i3 = 0; i3 < len; ++i3)
		{
			arr[++i2] = arr[i - 1];
		}
	}

	for (i = 0; i < endn; ++i)
	{
		arr[i] = arr[i2];
	}
	for (i = 0; i < endn; ++i)
	{
		cout << arr[i];
	}
}

void f128(int n, int k)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int len = 1, maxlen = 1, endmaxseries = 1;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len > maxlen) {

				maxlen = len;
				endmaxseries = i - 1;
			}
			len = 0;
		}
		++len;
	}
	if (len > maxlen)
	{
		maxlen = len;
		endmaxseries = i - 1;
	}

	for (i = ++n - 1; i > endmaxseries; --i)
	{
		arr[i] = arr[i - 1];
	}
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f129(int n, int k)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int len = 1, maxlen = 1, endmaxseries = 1;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len >= maxlen)
			{
				maxlen = len;
				endmaxseries = i - 1;
			}
			len = 0;
		}
		++len;
	}
	if (len > maxlen)
	{
		maxlen = len;
		endmaxseries = i - 1;
	}

	for (i = ++n - 1; i > endmaxseries; --i)
	{
		arr[i] = arr[i - 1];
	}
	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f130(int n, int k)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
	int len = 1, maxlen = 1, endmaxseries = 1;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len >= maxlen) maxlen = len;
			len = 0;
		}
		++len;
	}

	int i2;

	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] != arr[i])
		{
			if (len == maxlen)
			{
				for (i2 = ++n - 1; i2 > i; --i2)
				{
					arr[i2] = arr[i2 - 1];
				}
				++i;
			}
			len = 0;
		}
		++len;
	}

	for (i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
}

void f131(int n, int k)
{
	int i;
	int arr[20]{};
	for (int i = 0; i < n; ++i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}

}

void f3(int a, int d, int n)
{
	int arr[11]{};
	arr[0] = 1;
	for (int i = 0; i < n; i++)
	{
		arr[i] = a + (d * i);
		cout << arr[i] << endl;
	}
}

void f4(int a, int d, int n)
{
	int arr[11]{};
	for (int i = 0; i < n; i++)
	{
		arr[i] = a + pow(d, i);
		if (i == 0)
		{
			arr[0] -= 1;
		}
		cout << arr[i] << endl;
	}
}

void f5(int n)
{
	int arr[11]{};
	arr[0] = 1;
	arr[1] = 1;
	for (int i = 2; i < n; i++)
	{
		arr[i] = arr[i - 1] + arr[i - 2];
		cout << arr[i] << endl;
	}
}

void f6(int a, int b, int n)
{
	int arr[11]{};
	arr[0] = a;
	arr[1] = b;
	int sum = 0;
	for (int i = 0; i < n; i++)
	{

		if (i > 1)
		{
			arr[i] = sum;
		}
		sum += arr[i];
		cout << arr[i] << endl;
	}
}

void f7(int n)
{
	int arr[11]{};
	arr[10] = 11;
	for (int i = n; i > 0; --i)
	{
		arr[i] = i;
		cout << arr[i] << endl;
	}
}

void f8(int n)
{
	int count = 0;
	int arr[11]{};
	for (int i = 0; i <= n; i++)
	{
		arr[i] = i;
		if (arr[i] % 2 != 0)
		{
			count += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count;
}

void f9(int n)
{
	int count = 0;
	int arr[11]{};
	for (int i = n; i > 0; i--)
	{
		arr[i] = i;
		if (arr[i] % 2 == 0)
		{
			count += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count;
}

void f10(int n)
{
	int count1 = 0;
	int count2 = 0;
	int arr[11]{};
	for (int i = 0; i <= n; i++)
	{
		arr[i] = i;
		if (arr[i] % 2 == 0)
		{
			count1 += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count1 << endl;
	for (int i = n; i > 0; i--)
	{
		arr[i] = i;
		if (arr[i] % 2 != 0)
		{
			count2 += 1;
			cout << arr[i] << endl;
		}
	}
	cout << count2;
}

void f11(int n, int k)
{
	int arr[11]{ 1,5,8,7,9,6,8,7,3,6,5 };
	for (int i = 0; i <= n; i++)
	{
		if (arr[i] % k == 0)
		{
			cout << arr[i] << endl;
		}

	}
}
void f12(int n)
{
	int arr[11]{};
	for (int i = 0; i < n; i++)
	{
		if (i % 2 == 0)
		{
			cout << i << endl;
		}
	}
}
void f13(int* arr, int n)
{

	for (int i = 0; i < n; i++)
	{
		if (i % 2 != 0)
		{
			arr[i] = i;
			cout << i << endl;
		}
	}
}
void f14(int* arr, int n)
{

	for (int i = 0; i < n; i++)
	{
		if (i % 2 != 0)
		{
			arr[i] = i;
			cout << i << endl;
		}
	}
	for (int i = 0; i < n; i++)
	{
		if (i % 2 == 0)
		{
			arr[i] = i;
			cout << i << endl;
		}
	}
}
void f15(int* arr, int n)
{
	int i = 0;
	for (int i = 0; i < n; i++)
	{
		if (i % 2 != 0)
		{
			cout << i << endl;
		}
	}
	for (n; n != 0; n--)
	{
		if (n % 2 == 0)
		{
			cout << n << endl;
		}
	}
}
void f16(int* arr, int n)
{
	for (int i = 0; i < n; i++)
	{
		cout << i + 1 << endl;
	}
}
void f80(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int i = 0; i < n - 1; ++i)
	{
		arr[i] = arr[i + 1];
	}
		
	arr[n - 1] = 0;

	cout << "A:" << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
		

}
void f81(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i;
	for (i = n - 1; i > k - 1; --i)
	{
		arr[i] = arr[i - k];
	}
		
	for (; i >= 0; --i)
	{
		arr[i] = 0;
	}
		

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
}

void f82(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	for (int i = 0; i < n - k; ++i)
	{
		arr[i] = arr[i + k];
	}
		
	for (int i = 0; i < n; ++i)
	{
		arr[i] = 0;
	}
		

	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << arr[i];
	}
		

}

void f83(int* arr, int n, int k)

{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	double a0 = arr[n - 1];
	for (int i = n - 1; i >= 1; --i)
	{
		arr[i] = arr[i - 1];
	}
		

	arr[0] = a0;

	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
		

}
void f84(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	double a0 = arr[0];
	for (int i = 0; i < n - 1; ++i)
	{
		arr[i] = arr[i + 1];
	}
		
	arr[n - 1] = a0;
	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
		

}
void f85(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int ki, i;
	for (ki = 1; ki <= k; ++ki)
	{
		double a0 = arr[n - 1];
		for (i = n - 1; i >= 0; --i)
		{
			arr[i] = arr[i - 1];
		}
			
		arr[0] = a0;
	}

	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
		

}
void f86(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, ki;
	for (ki = 1; ki <= k; ++ki) 
	{
		float a0 = arr[0];
		for (i = 0; i < n - 1; ++i)
		{
			arr[i] = arr[i + 1];
		}
			
		arr[n - 1] = a0;
	}

	cout << "A: " << endl;
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i];
	}
		
}
void f87(int* arr, int n, int k)
{
	int at;
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int i = 1; i < n; ++i) 
	{
		if (arr[i - 1] > arr[i])
		{
			at = arr[i - 1];
			arr[i - 1] = arr[i];
			arr[i] = at;
		}
		else break;
	}
	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
		
}
void f88(int* arr, int n, int k)
{
	int at;
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int i = n - 2; i >= 0; --i) 
	{
		if (arr[i] > arr[i + 1])
		{
			at = arr[i - 1];
			arr[i - 1] = arr[i];
			arr[i] = at;
		}
		else break;
	}
	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}


}
void f89(int* arr, int n, int k)
{
	int at;
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int i = 1; i < n; ++i)
	{
		if (arr[i - 1] < arr[i]) 
		{
			at = arr[i - 1];
			arr[i - 1] = arr[i];
			arr[i] = at;
		}
	}
	cout << "A: " << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}


}

void f90(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i;
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << endl;
	}

	--n;

	for (i = k - 1; i < n; ++i)
	{
		arr[i] = arr[i + 1];
	}

	cout << "A:" << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i] << endl;
	}
}
void f91(int* arr, int n, int k, int l)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i;
	n -= l - k + 1;

	for (i = k - 1; i < n; ++i)
	{
		arr[i] = arr[i + (l - k + 1)];
	}

	cout << "A -" << n << endl;
	for (i = 0; i < n; ++i)
	{
		cout << arr[i] << endl;
	}
	
}
void f92(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int i = 0; i < n; ++i)
	{
		if (arr[i] % 2 == 0)
		{
			arr[k] = arr[i];
			++k;
		}
	}

	cout << "A" << endl;
	for (int i = 0; i < k; ++i)
	{
		cout << arr[i];
	}

}
void f93(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	for (int i = 0; i < n; i += 2)
	{
		arr[k] = arr[i];
		++k;
	}

	cout << "A -" << k << endl;
	for (int i = 0; i < k; ++i)
	{
		cout << arr[i] << endl;
	}
}
void f94(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	for (int i = 1; i < n; i += 2)
	{
		arr[n] = arr[i];
		++n;
	}

	cout << n << endl;
	for (int i = 0; i < n; ++i)
	{
		cout << arr[i] << endl;
	}


}
void f95(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int k = 0;
	for (int i = 1; i < n; ++i)
	{
		if (arr[k] != arr[i])
		{
			++k;
			arr[k] = arr[i];
		}
	}
	++k;

	cout << "A - " << k << endl;
	for (int i = 0; i < k; ++i)
	{
		cout << arr[i] << endl;
	}


}
void f96(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i2, k = 0;
	for (int i = 1; i < n; ++i)
	{
		arr[++k] = arr[i];
		for (i2 = 0; i2 < k; ++i2)
			if (arr[k] == arr[i2])
			{
				--k;
				break;
			}
	}
	++k;
	cout << "A - " << k << endl;
	for (int i = 0; i < k; ++i)
	{
		cout << arr[i] << endl;

	}

}
void f97(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i2, k = 0;
	for (int i = 0; i < n; ++i)
	{
		for (i2 = i + 1; i2 < n; ++i2)
		{
			if (arr[i2] == arr[i])
			{
				break;
			}
		}
		if (i2 == n)
		{
			arr[k] = arr[i];
			k++;
		}
	}
	cout << "A - " << k << endl;
	for (int i = 0; i < k; ++i)
	{
		cout << arr[i] << endl;
	}


}
void f98(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i2, k = -1, num, i;
	for (i = 0; i < n; ++i) 
	{
		for (i2 = 0; i2 <= k; ++i2)
		{
			if (arr[i] == arr[i2])
			{
				break;
			}
		}
		if (i2 != k + 1)
		{
			++k;
			arr[k] = arr[i];
		}
		else 
		{
			num = 0;
			for (i2 = i; i2 < n; ++i2)
			{
				if (arr[i2] == arr[i]) 
				{
					++num;

				}
			}
			if (num >= 3)
			{
				++k;
				arr[k] = arr[i];
			}
		}
	}
	++k;
	cout << "A - " << k << endl;
	for (i = 0; i < k; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}


}
void f99(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int ai, i2, k, num, i;
	for (i = 0; i < n; i++) {
		num = 0;
		for (i2 = 0; i2 < n; ++i2)
		{
			if (arr[i] == arr[i2]) ++num;
		}
		if (num > 2)
		{
			k = i - 1;
			ai = arr[i];
			for (i2 = i; i2 < n; ++i2)
			{
				if (arr[i2] != ai) 
				{
					++k;
					arr[k] = arr[i2];
				}
			}
				
			n = k + 1;
			--i;
		}
	}

	cout << "A -" << n << endl;
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f100(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int ai, i2, k, num, i;
	for (i = 0; i < n; i++)
	{
		num = 0;
		for (i2 = 0; i2 < n; ++i2)
			if (arr[i] == arr[i2]) ++num;

		if (num == 2)
		{
			k = i - 1;
			ai = arr[i];
			for (i2 = i; i2 < n; ++i2)
			{
				if (arr[i2] != ai)
				{
					++k;
					arr[k] = arr[i2];
				}
			}

			n = k + 1;
			--i;
		}
	}

	cout << "A - " << n << endl;
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}


}
void f101(int* arr, int k, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, k;
	n++;
	for (i = n - 1; i >= k; --i)
	{
		arr[i] = arr[i - 1];
	}


	arr[k - 1] = 0;

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f102(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i;
	n++;
	for (i = n - 1; i > k; --i)
	{
		arr[i] = arr[i - 1];
	}

	arr[k] = 0;


	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f103(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	int amin = 0, amax = 0, i;
	for (i = 0; i < n; ++i)
	{
		if (arr[amin] > arr[i]) {
			amin = i;
		}
		if (arr[amax] < arr[i]) {
			amax = i;
		}
	}
	if (amax > amin)
	{
		amax++;
	}
	n++;
	for (i = n - 1; i >= amin; --i)
	{
		arr[i] = arr[i - 1];
	}

	arr[amin] = 0;

	n++;
	for (i = n - 1; i > amax + 1; --i)
	{
		arr[i] = arr[i - 1];
	}

	arr[amax + 1] = 0;

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}


}
void f104(int* arr, int n)
{
	int n, k, m;
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	n += m;

	// Поочередно перемещаем элементы
	for (int i = n - 1; i >= k + m - 1; i--)
	{
		arr[i] = arr[i - m];
	}

	// Заполняем нулями
	for (int i = k - 1; i < k + m - 1; ++i)
	{
		arr[i] = 0;
	}

	// Выводим
	for (int i = 0; i < n; i++)
	{
		cout << arr[i] << " ";
	}

}
void f105(int* arr, int n, int k)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, m;
	for (i = n - 1; i >= k + m - 1; --i)
	{
		arr[i] = arr[i - m];
	}

	for (i = k - 1; i < k + m - 1; ++i)
	{
		arr[i] = 0;
	}


	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f106(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	int i2;
	for (int i = (n / 2) * 2 - 1; i >= 0; i -= 2)
	{
		++n;
		for (i2 = n - 1; i2 > i; --i2)
		{
			arr[i2] = arr[i2 - 1];
		}

	}

	for (int i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f107(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2, i3;
	for (i = n - ((n - (n / 2) * 2) - 1) - 1; i >= 0; i -= 2)
	{
		for (i3 = 1; i3 < 3; ++i3)
		{
			++n;
			for (i2 = n - 1; i2 > i; --i2)
			{
				arr[i2] = arr[i2 - 1];

			}
		}
	}
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;

	}

}
void f108(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2;
	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] > 0)
		{
			++n;
			for (i2 = n - 1; i2 > i; --i2)
			{
				arr[i2] = arr[i2 - 1];
			}
			arr[i] = 0;
		}
	}

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}
}

void f109(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2;
	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] < 0)
		{
			++n;
			for (i2 = n; i2 > i; --i2)
			{
				arr[i2] = arr[i2 - 1];

			}
			arr[i + 1] = 0;
		}
	}

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;

	}
}
void f110(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2;
	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] % 2 == 0)
		{
			++n;
			for (i2 = n - 1; i2 > i; --i2)
			{
				arr[i2] = arr[i2 - 1];

			}
		}
	}

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;

	}
}
void f111(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	int i, i2, i3;
	for (i = n - 1; i >= 0; --i)
	{
		if (arr[i] % 2 != 0)
		{
			for (i3 = 1; i3 < 3; ++i3)
			{
				++n;
				for (i2 = n - 1; i2 > i; --i2)
				{
					arr[i2] = arr[i2 - 1];

				}
			}
		}
	}

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;

	}

}
void f112(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2, i3;
	for (i = 0; i < n - 1; ++i)
	{
		for (i2 = 0; i2 < n - i; ++i2)
		{
			if (arr[i2] > arr[i2 + 1])
			{
				arr[i2] += arr[i2 + 1];
				arr[i2 + 1] = arr[i2] - arr[i2 + 1];
				arr[i2] -= arr[i2 + 1];
			}
		}
		for (i3 = 0; i3 < n; ++i3)
		{
			cout << i3 + 1 << arr[i3] << endl;

		}
		cout << endl;
	}

}
void f113(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2, i3, amax;
	for (i = n - 1; i > 0; --i)
	{
		amax = 1;
		for (i2 = 0; i2 <= i; ++i2)
		{
			if (arr[i2] > arr[amax])
			{
				amax = i2;
			}
		}
		if (i != amax)
		{
			arr[i] += arr[amax];
			arr[amax] = arr[i] - arr[amax];
			arr[i] -= arr[amax];
		}
	}
	for (i3 = 0; i3 < n; ++i3)
	{
		cout << i3 + 1 << arr[i3] << endl;

	}
	cout << endl;
}
void f114(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int temp;
	if (arr[0] > arr[1])
	{
		temp = arr[0];
		arr[0] = arr[1];
		arr[1] = temp;
	}
	int i, i2, i3;

	for (i = 2; i <= n - 1; ++i)
	{
		temp = arr[i];
		for (i2 = i - 1; i2 >= 0; --i2)
		{
			if (temp < arr[i2])
			{
				arr[i2 + 1] = arr[i2];

			}
			else
			{
				break;
			}
		}

		arr[i2 + 1] = temp;
		for (i3 = 0; i3 < n; ++i3)
		{
			cout << i3 + 1 << arr[i3] << endl;

		}
		cout << endl;
	}
}
void f115(int* arr, int n )
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2, i3, i4;
	for (i4 = 0; i4 < n; ++i4)
	{
		for (i2 = 0; i2 <= n - i4 - 2; ++i2)
		{
			if (arr[arr[i2]] > arr[arr[i2] + 1])
			{
				arr[i2] += arr[i2 + 1];
				arr[i2 + 1] = arr[i2] - arr[i2 + 1];
				arr[i2] -= arr[i2 + 1];
			}
		}
		for (i3 = 0; i3 < n; ++i3)
		{
			cout << arr[i3];
		}
	}
}
void f116(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int  b[10], c[10];
	int i, k = 0;
	b[k] = 1;
	c[k] = arr[k];
	for (i = 1; i < n; ++i)
	{
		if (arr[i - 1] == arr[i])
			++b[k];
		else {
			++k;
			b[k] = 1;
			c[k] = arr[i];
		}
	}
	for (i = 0; i <= k; ++i)
	{
		cout << i + 1 << b[i] << " " << c[i] << " " << endl;

	}
}
void f117(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int b[10];
	int k = 1;
	b[0] = 0;
	b[k] = arr[1];
	for (int i = 1; i < n; ++i) 
	{
		++k;
		if (arr[i - 1] != arr[i])
		{
			b[k] = 0;
			++k;
		}
		b[k] = arr[i];
	}

	for (int i = 0; i <= k; ++i)
	{
		arr[i] = b[i];

	}

	for (int i = 0; i <= k; ++i)
	{
		cout << i + 1 << arr[i] << endl;

	}
}
void f118(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}

	int i, i2;
	for (i = 0; i < n; ++i)
	{
		if (i + 1 < n)
		{
			if (arr[i + 1] != arr[i])
			{
				++n;
				for (i2 = n - 1; i2 > i; --i2)
				{
					arr[i2] = arr[i2 - 1];

				}
				++i;
				arr[i] = 0;

			}
		}
	}
	++n;
	arr[n - 1] = 0;

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;

	}
}
void f119(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2;
	for (i = 0; i < n; ++i) {
		if (i + 1 < n) {
			if (arr[i + 1] != arr[i])
			{
				++n;
				for (i2 = n - 1; i2 > i; --i2)
				{
					arr[i2] = arr[i2 - 1];
				}
				++i;
			}
		}
	}
	++n;
	arr[n - 1] = arr[n - 2];

	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f120(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
	int i, i2;
	for (i = 0; i < n; ++i)
	{
		if (i + 1 < n)
		{
			if (arr[i] != arr[i + 1])
			{
				--n;
				for (i2 = i; i2 < n; ++i2)
					arr[i2] = arr[i2 + 1];
				--i;
			}
		}
	}
	--n;
	for (i = 0; i < n; ++i)
	{
		cout << i + 1 << arr[i] << endl;
	}

}
void f131(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f132(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f133(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f134(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f135(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f136(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f137(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f138(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f139(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}
void f140(int* arr, int n)
{
	for (int a = 0; a < n; ++a)
	{
		arr[a] = a;
		cout << arr[a] << endl;
	}
}

int main()
{
	const int size = 10;
	int arr[size];
	//f1_1(10);
	//f1_2(10);
	//f2(10);
	//f3(10,5,10);
	//f4(10,5,10);
	//f5(11);
	//f6(2, 5, 11);
	//f7(10);
	//f8(10);
	//f9(10);
	//f10(10);
	//f11(10,2);
	//f12(10);
	//f13(arr, size);
	//f14(10);
	//f15(10);
	//f16(11);
	//f17(10);
	//f18(10);
	//f19(11);
	//f20(10,5,10);
	//f21(10,5,10);
	//f22(10,5,10);
	//f23(10,5,10);
	//f24(10);
	//f25(10);
	//f26(10);
	//f27(10);
	//f28(10);
	//f29(10);
	//f30(10);
	//f31(10);
	//f32(10);
	//f33(10);
	//f34(10);
	//f35(10);
	//f36(10);
	//f37(10);
	//f38(10);
	//f39(10);
	//f40(10,5);
	//f41(10);
	//f42(10);
	//f43(10);
	//f44(10);
	//f45(10);
	//f46(10);
	//f47(10);
	//f48(10);
	//f49(10);
	//f50(10);
	//f51(10);
	//f52(10);
	//f53(10);
	//f54(10);
	//f55(10);
	//f56(10);
	//f57(10);
	//f58(10);
	//f59(10);
	//f60(10);
	//f61(10);
	//f62(10);
	//f63(10);
	//f64(10);
	//f65(10);
	//f66(10);
	//f67(10);
	//f68(10);
	//f69(10);
	//f70(10);
	//f71(10);
	//f72(10,5,10);
	//f73(10,5,10);
	//f74(10);
	//f75(10);
	//f76(10);
	//f77(10);
	//f78(10);
	//f79(10);
	//f80(10);
	//f120(10);
	//f121(10,10);
	//f122(10,10);
	//f123(10,10);
	//f124(10);
	//f125(10,10);
	//f126(10,10);
	//f127(10,10);
	//f128(10,10);
	//f129(10,10);
	//f130(10,10);
	//d(size, arr);
	const int size = 11;
	int arr[size];
	//f80(arr, size, 10);
	//f81(arr, size, 10);
	//f82(arr, size, 10);
	//f83(arr, size, 10);
	//f84(arr, size, 10);
	//f85(arr, size, 10);
	//f86(arr, size, 10);
	//f87(arr, size, 10);
	//f88(arr, size, 10);
	//f89(arr, size, 10);
	//f4(10,5,10);
	//f5(11);
	//f6(2, 5, 11);
	//f7(10);
	//f8(10);
	//f9(10);
	//f10(10);
	//f11(10,2);
	//f12(10);
	//f13(arr, size);
	//f14(arr, size);
	//f15(arr, size);
	//f16(arr, size);
	//f90(arr, size,10);
	//f91(arr, size, 10,1);
	//f92(arr, size, 10);
	//f93(arr, size, 10);
	//f94(arr, size);
	//f95(arr, size);
	//f96(arr, size);
	//f97(arr, size);
	//f98(arr, size);
	//f99(arr, size);
	//f100(arr, size);
	//f101(arr, size,5);
	//f102(arr, size,5);
	//f103(arr, size);
	//f104(arr, size);
	//f105(arr, size,5); 
	//f106(arr, size);
	//f107(arr, size);
	//f108(arr, size); 
	//f109(arr, size);
	//f109(arr, size);
	//f110(arr, size);
	//f111(arr, size);
	//f112(arr, size);
	//f113(arr, size);
	//f114(arr, size);
	//f115(arr, size);
	//f116(arr, size);
	//f117(arr, size);
	//f118(arr, size);
	//f119(arr, size);
	//f120(arr, size);
	return 0;
}
