struct candidate{
	char code [5];
	char name[30];
	double math,physics,chemitry,markAvg;
};

typedef struct candidate CDD;

float diemTB(CDD x){
	return(x.math+x.physics+x.chemitry)/3;
}

void input(CDD *x){
	rewind(stdin);
	printf("\nCode: ");
	gets(x->code);
	printf("\nFull Name: ");
	gets(x->name);
	printf("\nMath, Physics, Chemistry: ");
	scanf("%lf %lf %lf", &x->math, &x->physics, &x->chemitry);
}
void output(CDD x){
	printf("\nCode: %s",x.code);
	printf("\nFull Name: %s",x.name);
	printf("\nMath: %.2lf, Physics: %.2lf, Chemitry: %.2lf",x.math,x.physics,x.chemitry);
	printf("\nMark Average: %.2lf", diemTB(x));
}

int main(){
	CDD st1;
	printf("\nPlease fill the information: ");
	input(&st1);
	printf("\n----- Information -----");
	output(st1);
}
