<h2>Notes</h2>

```
// Lam tron
#include<cmath>
roundf(kq*100)/100; // Lam tron den STP thu 2
roundf(kq*1000)/1000; // Lam tron den STP thu 3

// Lam tron 0.5
int lamTron(double a)
{
	int h;
		if ((a-int(a))>=0.5)
			h=int(a)+1;
		else h=int(a);
	return h;
}

// Thao tac chuoi
// Noi chuoi
c=a+b;
// Noi chuoi (tai vi tri chi dinh)
s.insert(position, string);
// So sanh
s1.compare(s2);
// Hoan doi chuoi
s1.swap(s2);
// Tim vi tri chuoi con
s1.find(s1);
// Thay the tai vi tri chi dinh
s.replace(position, amount, string);
// Xoa cac ky tu trong pham vi chi dinh
a.erase(position, amount);
// Tach chuoi
b=substr.a(position, amount);
// Tach tung tu trong chuoi (phan biet boi dau cach)
stringstream ss(a);
// "tu do hanh phuc" -> "ut od hnah cuhp"
void daoChuoi()
{
	string a;
	getline(cin,a);
	stringstream ss(a);
	string tmp;
	while(ss >> tmp)
	{
		reverse(tmp.begin(),tmp.end());
		cout<<tmp<<" ";
	}
	
	// Luu chuoi
	string c;
	while(ss >> tmp)
		c+=tmp+" ";
}

// Chuyen chuoi ky tu thanh so
int changeToNum(string s)
{
	int value = 0;
	for (int i = 0; i < s.size(); i++)
		value = value * 10 + (s[i] - '0');
	return value;
}

// Chuyen so thanh chuoi ky tu
string changeToString(int value)
{
	string result = "";
	if (value == 0)
		return "0";

	while (value > 0)
	{
		result = (char)('0' + value % 10) + result;
		value /= 10;
	}
	return result;
}

// Thao tac mang
// Mang 2 chieu thanh mang 1 chieu
void mang2thanh1chieu(int A[][SIZE], int m, int n, int B[])
{
	int nB=0;
	for(int i=0;i<m;i++)
		for(int j=0;j<n;j++)
			B[nB++]=A[i][j];
}

// Mang 1 chieu thanh mang 2 chieu
void mang1thanh2chieu(int A[][SIZE], int m, int n, int B[])
{
	int nB=0;
	for(int i=0;i<m;i++)
		for(int j=0;j<n;j++)
			A[i][j]=B[nB++];
}

// Chen x vao k
void chenXvaoK(int A[], int &n, int x, int k)
{
	for(int i=n-1;i>=k;i--)
		A[i+1]=A[i];
	A[k]=x;
	n++;
}

// Xoa vi tri k
void xoaViTriK(int A[], int &n, int k)
{
	for(int i=k;i<n-1;i++)
		A[i]=A[i+1];
	n--;
}

// Ghep mang xen ke
void ghepMangXenKe(nt &nC, int C[])
{
	int iA=0;
	int iB=0;
	nC=0;
	while(iA<nA && iB<nB)
	{
		C[nC++]=A[iA++];
		C[nC++]=B[iB++];
	}
	while(iA<nA)
		C[nC++]=A[iA++];
	while(iB<nB)
		C[nC++]=B[iB++];
}

// Tong so trong chuoi
int tongSoTrongChuoi(char A[])
{
	int n=strlen(A);
	int s=0;
	int num=0;
	for(int i=0;i<=n;i++)
		if(A[i]>='0'&&A[i]<='9')
			num=num*10+(A[i]-'0');
		else
		{
			s+=num;
			num=0;
		}
	return s;	
}

// Lat nguoc mang
void latNguoc(char A[], int x, int y)
{
	while(x<y)
	{
		char tmp=A[x];
		A[x]=A[y];
		A[y]=tmp;
		x++;
		y--;
	}
}

// Doi he 2 sang he 10
int doiHe2SangHe10(char S[])
{
	int s=0;
	for (int i=0;i<strlen(S);i++)
		s+=pow(2,i)*(S[i]-'0');
	return s;
}

// Doi tu he 10 sang he 2, 8, 16
void doiHe(int n, char S[], int he)
{
	char x[]={'0','1','2','3','4','5','6',
	'7','8','9','A','B','C','D', 'E','F'};
	int i=0;
	while(n>0)
	{
		S[i]=x[n%he];
		n /= he;
		i++;
	}
	S[i]='\0';
	strrev(S);
}

// Ngay lien sau 1 ngay
void ngayLienSau1ngay(int &d, int &m, int &y)
{
	d++;
	if(d>tinhNgayTrongThang(m,y))
	{
		d=1;
		m++;
		if(m>12)
		{
			m=1;
			y++;
		}
	}
}

// Ngay thu bao nhieu trong nam
int soNgayThuBaoNhieuTrongNam(int d, int m, int y)
{
	int dem=d;
	for(int i=1; i< m; i++)
		dem= dem + tinhNgayTrongThang(i,y);
	return dem;
}

// Tinh ngay trong NAM
int soNgayTrongNam(int y)
{
	if(ktNamNhuan(y)==1)
		return 366;
	else
		return 365;
}

// Ngay - thang - nam Hop le
bool hopLe(int d, int m, int y)
{
	return d>0 && d<=tinhNgayTrongThang(m,y) && m>0 && m<13 && y>0;
}

// Kiem tra NAM NHUAN
bool ktNamNhuan(int y)
{ 
	return( y>0 && (y % 4 == 0 && y % 100 != 0 || y % 400 == 0) );
}

// Tinh NGAY trong thang
int tinhNgayTrongThang(int m, int y)
{
	if(m==4||m==6||m==9||m==11)
		return 30;
	else 
		if(m==2)
		{
			if(ktNamNhuan(y))
				return 29;
			else 
				return 28;
		}
		else 
			return 31;
}

// Tim x (linh canh)
int timX(int A[], int n, int x)
{
	A[n]=x;
	int i=0;
	while(A[i]!=x)
		i++;
	if(i<n)
		return 1;
	else
		return -1;
}

// Tim x nhi phan (mang tang dan)
int timXnhiPhan(int A[], int n, int x)
{
	int r,l;
	r=n-1;
	l=0;
	
	for(int i=l;i<r;i++)
	{
		int mid= (l+r-1)/2;
		if(A[mid]==x)
			return mid;
		else
			if(A[mid]>x)
				r=mid-1;
			else
				l=mid+1;	
	}
	return -1;
}

// Tim x nhi phan (de quy)
int timX(int A[], int left, int right, int x)
{
	if(right>=left)
	{
		int mid=left+(right-left)/2;
		if(A[mid]==x)
			return mid;
		else
			if(A[mid]>x)
				return timX(A,left,mid-1,x);
			else
				return timX(A,mid+1,right,x);
	}
	return -1;
}

// To hop (de quy)
int toHop(int k, int n)
{
	if(k==0||k==n)
		return 1;
	if(k==1)
		return n;
	else
		return toHop(k-1,n-1)+toHop(k,n-1);
}

// Tim UCLN cua 2 so
int UCLN(int a, int b)
{
	a=abs(a);
	b=abs(b);
	while(a!=b)
	{
		if (a>b)
			a-= b;
		else
			b-= a;
	}
	return a;
}

// Boi chung lon nhat cua 2 so
int BCNN(int a, int b)
{
	return a*b/UCLN(a,b);
}

// Xuat ra SO DAO NGUOC cua n
int reverse(int n)
{
	int rev=0;
	for(int r; n>0; n=n/10)
	{
		r = n%10;
		rev = rev*10 +r;	
	}
	return rev;
}

// Kiem tra n TANG DAN
int ktTangDan(int n)
{
	int cuoi=n%10;
	n /= 10;
	while(n!=0)
	{
		int keCuoi=n%10;
		n /=10;
		if(keCuoi<cuoi)
			cuoi=keCuoi;
		else
			return 0;
	}
	return 1;
}

// Kiem tra SO NGUYEN TO
bool ktSNT(int n)
{
	if(n<2)
		return 0;
	for(int i=2; i<=sqrt(n); i++)
		if(n%i == 0)
			return 0;
	return 1;
}

// Kiem tra SO HOAN HAO
bool ktSHH(int n)
{
	int s=0;
	for(int i=1; i<= n/2; i++)
	{
		if (n%i == 0)
			s+= i;
	}
	if (s==n)
		return 1;
	else
		return 0;
}

// Kiem tra SO CHINH PHUONG
bool ktSCP(int n)
{
	int i=0;
	while(i*i <=n)
	{
		if(i*i==n)
			return 1;
		i++;
	}
	return 0;
}

// Phan tich THUA SO NGUYEN TO
int phanTichThuaSoNguyenTo(int n)
{
	int dem;
	for(int i=2; i<=n; i++)
	{
		dem=0;
		while(n % i == 0)
		{
			dem++;
			n /= i;
		}
		if(dem!=0)
		{
			cout << i;
			if(dem > 1) 
				cout <<"^"<< dem;
			if(n > i)
				cout <<" * ";
		}
	}
}

// Day FIBONACCI
int dayFibonacci(int n)
{
	int f1=1;
	int fn=1;
	if (n==0 || n==1) 
		return n;
	else
		for(int i=2; i<n; i++)
		{
			int f0=f1;
			f1=fn;
			fn=f0+f1;
		}
	return fn;
}

// fibo (de quy)
int fibo(int n)
{
	if (n==0 || n==1) 
		return 1;
	else
		return fibo(n-2)+fibo(n-1);
}

// fibo so lon
string fibo(int n)
{
	if(n==0)
		return "0";
	else
		if(n==1)
			return "1";
	
	string a="0";
	string b="1";
	string c="";
	for(int i=2;i<=n;i++)
	{
		c=tong2soLon(a,b);
		a=b;
		b=c;
	}
	return c;
}

// Tim min (de quy)
int min(int A[], int n)
{
	if(n==0)
		return -1;
	if(n==1)
		return A[0];
	else
		if(A[n-1]<min(A,n-1))
			return A[n-1];
		else
			return min(A,n-1);
}

// Tong mang 1 chieu (de quy)
int tong(int A[], int n)
{
	if(n==0)
		return 0;
	else
		return A[n-1]+tong(A,n-1);
}

// Giai thua (de quy)
int giaiThua(int n)
{
	if(n==0)
		return 1;
	else
		return n*giaiThua(n-1);
}

// Tinh x mu p (de quy)
int tinhXmuP(int x, int p)
{
	if(p==1)
		return x;
	else
		return x*tinhXmuP(x,p-1);
}

// Tong 2 so lon
string tong2soLon(string a, string b)
{
	while(a.size()<b.size())
		a="0"+a;
	while(b.size()<a.size())
		b="0"+b;
	reverse(a.begin(),a.end());
	reverse(b.begin(),b.end());
	
	int t=0;
	int nho=0;
	string s="";
	
	for(int i=0;i<a.size();i++)
	{
		t=(a[i]-'0') + (b[i]-'0') + nho;
		s+= t%10 + '0';
		nho= t/10;
	}
	
	if(nho==1)
		s+="1";
	reverse(s.begin(),s.end());
	return s;
}

// Hieu 2 so lon
string hieu2soLon(string a, string b)
{
	while(a.size()<b.size())
		a="0"+a;
	while(b.size()<a.size())
		b="0"+b;
	reverse(a.begin(),a.end());
	reverse(b.begin(),b.end());
	
	string c;
	int t=0;
	int nho=0;
	
	for(int i=0;i<a.size();i++)
	{
		t=(a[i]-'0') -(b[i]-'0') -nho;
		if(t<0)
		{
			c+=t+10 +'0';
			nho=1;
		}
		else
		{
			c+=t +'0';
			nho=0;
		}
	}
	
	reverse(c.begin(),c.end());
	if(c[0]=='0')
		return "0";
	else
		return c;
}

// Tich 2 so lon
string tich2soLon(string a, string b)
{
	while(a.size()<b.size())
		a="0"+a;
	while(b.size()<a.size())
		b="0"+b;
	reverse(a.begin(),a.end());
	reverse(b.begin(),b.end());
	
	string c;
	for(int k=0;k<a.size()+b.size();k++)
		c+="0";
	
	for(int iB=0;iB<b.size();iB++)
	{
		int nho=0;
		int iA;
		for(iA=0;iA<a.size();iA++)
		{
			int x= (b[iB]-'0')*(a[iA]-'0') + nho + (c[iA+iB]-'0');
			c[iA+iB]= x%10 +'0';
			nho= x/10;
		}
		if(nho>0)
			c[iA+iB]=nho + '0';
	}
	reverse(c.begin(),c.end());
	while(c[0]=='0')
		c.erase(0,1);
	return c;
}

// Số lớn chia số nhỏ
// <num> là số cần chia, <numlen> là độ dài của số cần chia
string divide (string a)
{
	if ((int)a.size() < <numlen> && changeToNum(a) < <num>)
		return "0";
	string ans = "";
	int res = 0;
	for (int i = 0; i < a.size(); i++) {
		int tmp = res * 10 + (a[i] - '0');
		ans += changeToString(tmp / <num>);
		res = tmp % <num>;
	}
	while (ans[0] == '0') ans.erase(0, 1);
	return ans;
}

// So sanh 2 chuoi
int soSanh(string a, string b)
{
	if(a.size()>b.size())
		return 1;
	else
		if(a.size()<b.size())
			return -1;
		else
			if(a>b)
				return 1;
			else
			{
				if(a<b)
					return -1;
				else
					return 0;
			}
}

// Dem phan tu trung
void demTanSuatTungKyTu(char A[], int n)
{
	for(int i=0;i<n;i++)
	{
		bool kt=1;
		for(int j=i-1;j>=0;j--)
		{
			if(A[i]==A[j])
			{
				kt=0;
				break;
			}
		}
		if(kt==1)
		{
			int dem=0;
			for(int k=0;k<n;k++)
			{
				if(A[i]==A[k])
					dem++;
			}
			cout<<A[i]<<": "<<dem<<endl;
		}
	}
}

// Liet ke nhi phan (de quy)
void lietKeNhiPhan(int k)
{
	if(k==n)
		xuat();
	else
	{
		for(int i=0;i<=1;i++)
		{
			A[k]=i;
			lietKeNhiPhan(k+1);
		}
	}
}

// Sinh nhi phan
void sinhNhiPhan(int n)
{
	int A[SIZE]={0};
	int i;
	do
	{
		i=n-1;
		xuat(A,n);
		while(i>=0 && A[i]==1)
		{
			A[i]=0;
			i--;
		}
		if(i>=0)
			A[i]=1;
	}
	while(i>=0);
}

// Liet ke tap con (de quy)
void lietKeTapCon(int k)
{
	if(k==n)
		xuat();
	else
	{
		for(int i=0;i<=1;i++)
		{
			A[k]=i;
			lietKeTapCon(k+1);
		}
	}	
}

// Sinh tap con
void sinhTapCon()
{
	int A[SIZE]={0};
	int k=0;
	int i=0;
	xuat(A,k);
	k=1;
	
	do
	{
		xuat(A,k);
		if(A[i]<n-1)
		{
			A[i+1]=A[i]+1;
			i++;
			k++;
		}
		else
		{
			if(i==0)
				break;
			i--;
			k--;
			A[i]++;
		}
	}
	while(true);
}

// Liet ke hoan vi (de quy)
void lietKeHoanVi(int k)
{
	if(k==n)
		xuat();
	else
	{
		for(int i=0;i<n;i++)
		{
			if(B[i]==0)
			{
				A[k]=i;
				B[i]=1;
				lietKeHoanVi(k+1);
				B[i]=0;
			}
		}
	}
}

// Sinh hoan vi
void sinhHoanVi(int A[], int n)
{
	xuat(A,n);
	do
	{
		int k=n-2;
		while(k>=0 && A[k]>A[k+1])
			k--;
		if(k<0)
			break;
		int l=n-1;
		while(A[l]<A[k])
			l--;
		doiCho(A[k],A[l]);
		latNguoc(A,k+1,n-1);
		xuat(A,n);
	}
	while(true);
}

// Nguoi di du lich - tinh chi phi toi uu
void tinhChiPhi()
{
	int chiPhi=0;
	for(int i=0;i<n-1;i++)
		chiPhi+=C[A[i]][A[i+1]];
	chiPhi+=C[A[n-1]][A[0]];
	if(chiPhi<chiPhiToiUu)
	{
		chiPhiToiUu=chiPhi;
		for(int i=0;i<n;i++)
			H[i]=A[i];
	}
}

// Phan cong viec - thoi gian toi uu
void tgTU()
{
	int ta=0;
	int tb=0;
	for(int i=0;i<n;i++)
		if(P[i]==0)
			ta+=A[i];
		else
			tb+=B[i];
	int tg=ta;
	if(ta<tb)
		tg=tb;
	if(tg<tgtu)
	{
		tgtu=tg;
		for(int i=0;i<n;i++)
			H[i]=P[i];
	}
}

// dau ngoac "(,)"
int tinhDoSau()
{
	int mongoac=0;
	int dosau=0;
	int i=0;
	while(i<m)
	{
		if(A[i]==0)
			mongoac++;
		else
		{
			if(mongoac==0)
				return -1;
			if(mongoac>dosau)
				dosau=mongoac;
			mongoac--;
		}
		i++;
	}
	if(mongoac==0)
		return dosau;
	else
		return -1;
}

// check so Amstrong
bool laSoAmstrong(int n)
{
	int k=demChuSo(n);
	int s=0;
	int cpy=n;
	while(n>0)
	{
		int tmp=n%10;
		s+=tinhXmuP(tmp,k);
		n/=10;
	}
	if(s==cpy)
		return 1;
	else
		return 0;
}

// kiem tra vi tri yen ngua
bool ktYenNgua(int A[][SIZE], int m, int n, int x, int y)
{
	int tam=A[x][y];
	
	//max hang
	for(int j=0;j<n;j++)
		if(tam<A[x][j])
			return 0;
	
	//min cot
	for(int i=0;i<m;i++)
		if(tam>A[i][y])
			return 0;
	
	return 1;
}

// Tinh F(n). Voi F(0)=0, F(1)=1, F(2n)=F(n), F(2n+1) = F(n) + F(n+1)
// De quy
int tinhFn(int n)
{
	if(n==0||n==1)
		return n;
	if(n%2==0)
		return tinhFn(n/2);
	else
		return tinhFn((n-1)/2) + tinhFn((n+1)/2);
}

// Mang F(n)
int tinhFn(int A[], int n)
{
	A[0]="0";
	A[1]="1";
	for(int i=1;i<=n;i++)
	{
		A[2*i]=A[i];
		A[2*i+1]=A[i] + A[i+1];
	}
	return A[n];
}

// Liet ke cac mang con tang dan
// 6 5 3 2 3 4 2 7 -> [2 3 4; 2 7]
void lietKeMangConTangDan(int A[], int n)
{
	int B[SIZE],nb=0;
	for(int i=0;i<n;i++)
	{
		B[nb++]=A[i];
		if(i==n-1 || A[i]>A[i+1])
		{
			if(nb>1)
				xuat(B,nb);
			nb=0;
		}
	}
}

// Tam giac pascal (de quy)
int pascal(int k, int n)
{
	if(k==0||k==n)
		return 1;
	else
		return pascal(k-1,n-1) + pascal(k,n-1);
}

void tamGiacPascal(int n)
{
	for(int i=0;i<=n;i++)
	{
		for(int k=0;k<=i;k++)
			cout<<setw(5)<<pascal(k,i);
		cout<<endl;
	}
}

// Tim day don dieu dai nhat
int timMax(int A[], int a, int b)
{
	int max=A[a];
	for(int i=a;i<b;i++)
		if(A[i]>=max)
			max=A[i];
	return max;
}

void ganMang(int A[], int n, int L[])
{
	for(int i=0;i<=n+1;i++)
	{
		int max=timMax(L,i+1,n+1);
			for(int j=i+1;j<=n+1;j++)
			{
				if(L[j]==max && A[j]>=A[i])
				{
					cout<<A[j]<<" ";
					break;
				}
			}
	}
}

void quyHoachDong(int A[], int n, int L[])
{
	for(int i=n+1;i>=0;i--)
	{
		L[i]=1;
		for(int j=i+1;j<=n+1;j++)
		{
			if((i==0 || j==n+1 || A[i]<=A[j]) && L[i]<L[j]+1)
				L[i]=L[j]+1;
		}
	}
}

void quyHoachDong(char A[], char B[], int nA, int nB, int L[][SIZE])
{
    for (int i = 0; i <= nB; i++)
        L[i][0] = 0;
    for (int i = 0; i <= nA; i++)
        L[0][i] = 0;
    for (int i = 0; i < nB; i++)
    {
        for (int j = 0; j < nA; j++)
        {
            if (A[j] == B[i])
                L[i + 1][j + 1] = L[i][j] + 1;
            else
                L[i + 1][j + 1] = timMax(L[i][j + 1], L[i + 1][j]);
        }
    }
}

// Tim xau con chung dai nhat
void xuLy(char A[], char B[], int nA, int nB, int L[][SIZE])
{
    char T[SIZE];
    int nt = 0;
    int i = nB;
    int j = nA;
    while (true)
    {
        if (A[j - 1] == B[i - 1])
        {
            T[nt] = A[j - 1];
            i--;
            j--;
            nt++;
        }
        else
        {
            if (timMax(L[i - 1][j], L[i][j - 1]) == L[i - 1][j])
                i--;
            else
                j--;
        }
        if (L[i][j] == 0)
            break;
    }
    T[nt] = '\0';
    strrev(T);
    puts(T);
}

// &1 = chính nó, &0 = 0
// |0 = chính nó, |1 = 1
// ^: giống = 0, khác = 1
// ~: 0 = 1, 1 = 0;

// Dịch trái (n<<k = n*2^k) (đuôi thêm 0)
// Dịch phải (n>>k = n/2^k) (đầu thêm bit trái cùng)

int layBit(int n, int k)
{
    return (n >> k) & 0x1;
}

void batBit(int &n, int k)
{
    n = n | (0x1 << k);
}

void tatBit(int &n, int k)
{
    n = n & (~(0x1 << k));
}

int dichTraiXoayVong(int n, int k)
{
    int a = 0x1;
    for (int i = 0; i < k; i++)
        batBit(a, i);
    return ((n >> 32 - k) & a) | (n << k);
}

int demBit1(int n, int dem, int he)
{
    for (int i = 0; i < he; i++)
    {
        if (layBit(n, i) == 1)
            dem++;
    }
    return dem;
}

```
