#include <iostream>
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <fstream>
#include <string>
#include <limits>

int z(0);
int a(0);
int e(0);
int h(0);
unsigned int f(0);
unsigned int q(0);

using namespace std;

int main()
{
    string ligne;
    string monFlux;
    char lineornot;

    cout << "demarrage super programme de la mort qui tue un bebe phoque :P " <<endl;
    cout << "appuyé sur m si on veut demarrer à une ligne precise sinon q "<<endl ;
    cin >> lineornot ;

    ifstream fichier("D:/2nd/lien.txt");

    if(fichier)
    {
        int lines = 0;
        while ( fichier.ignore( numeric_limits<int>::max(), '\n' ) )
        {
            ++lines;
        }
        cout<<lines<<endl;
        f=lines;
        cout<<"f ="<<f<<endl;
        //L'ouverture s'est bien passée, on peut donc lire
        if (lineornot == 'm')
        {
            a=0;
            cout << "je veux demarrer a la ligne : ";
            cin >> z;
            while (a!=z)
            {
                a++;
                cout<<a<<endl;
                getline(fichier, ligne);
            }
            system(("start "+ligne).c_str());
        }
        if (lineornot =='q')
        {
            cout<< "rentre dans le if q"<<endl;
            while (lines>=h)
            {
                cout<<"valeur de f"<<f;
                q=f-(f-10);
                f=f-10;
                cout << "valeur de q ="<<q<<endl;
                e=0;
                while (e<q)
                {
                    h++;
                    cout<< "valeur de h ="<<h<<endl;
                    e++;
                    cout<< "valeur de e ="<<e<<endl;
                    getline(fichier, ligne); //On lit une ligne complète
                    cout<<ligne<<endl;
                    system(("start "+ligne).c_str());
                    Sleep(1000);
                }
                Sleep(1000);

            }
        }
    }
    else
    {
      cout << "ERREUR: Impossible d'ouvrir le fichier en lecture." << endl;
    }
    cout<<"fin";
    return 0;
}
