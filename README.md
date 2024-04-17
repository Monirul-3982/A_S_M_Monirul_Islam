// A_S_M_Monirul_Islam
#include<stdio.h>
int main()
{
    double side[3], temp;
    int i, j;
    for(i=0; i<3; i++) {
        scanf("%lf", &side[i]);
    }
    for(i=0; i<3; i++) {
        for(j=i+1; j<3; j++) {
            if(side[i]<side[j]) {
                temp=side[i];
                side[i]=side[j];
                side[j]=temp;
            }
        }
    }
    double a=side[0], b=side[1], c=side[2];
    if(a>=b+c) {
        printf("NAO FORMA TRIANGULO\n");
        return 0;
    }
    if(a*a==b*b+c*c) printf("TRIANGULO RETANGULO\n");
    if(a*a>b*b+c*c) printf("TRIANGULO OBTUSANGULO\n");
    if(a*a<b*b+c*c) printf("TRIANGULO ACUTANGULO\n");
    if(a==b && b==c && a==c) printf("TRIANGULO EQUILATERO\n");
    if(a==b && a!=c && b!=c || a==c && a!=b && c!=b || b==c && b!=a && c!=a) printf("TRIANGULO ISOSCELES\n");
    return 0;
}
