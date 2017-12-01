# third-point
using namespace std;

int main(int argc, char *argv[])
{
    system("PAUSE");
    int m;
    cout<<"introduce el tamaño del arreglo ";
    cin>> m;
    int impar = 0;
    int par = 0;
    int negativo=0;
    int positivo=0;
    int arreglo[m][m];
    int impares[impar][impar];
    int pares[par][par];
    int positivos[positivo][positivo];
    int negativos[negativo][negativo];
    for(int i = 0; i < m; i=i+1){
            for(int j=0; j<m; j=j+1){
                    arreglo[i][j]=(rand()%101) -50;
                    if(arreglo[i][j]% 2 == 0){
                             par = par + 1;
                             pares[i][j] = abs(arreglo[i][j]);
                             cout << "el numero " << pares[i][j]<< " es par"  << endl;
                    }else{

                          if(arreglo[i][j]% 2 == 1){
                                               impar = impar + 1;
                                               impares[i][j] = abs(arreglo[i][j]);
                                               cout << "el numero " << impares[i][j]<<" es impar"  << endl;
                          }
                    }
                    if(arreglo[i][j]<0){
                             negativo = negativo + 1;
                             negativos[i][j] =arreglo[i][j];
                             cout << "el numero " << negativos[i][j] << " es negativo"  << endl;
                    }else{

                          if(arreglo[i][j] > 0){
                                           positivo = positivo + 1;
                                           positivos[i][j] = abs(arreglo[i][j]);
                                           cout << "el numero "  << positivos[i][j] << " es positivo" << endl;
                          }
                    }
            }
    }
    cout << "hay " << par << " numeros pares" << endl;
    cout << "hay " << impar << " numeros impares" << endl;
    cout << "hay " << negativo << " numeros negativos" << endl;
    cout << "hay " << positivo <<  " numeros positivos" << endl;

    return EXIT_SUCCESS;
}
