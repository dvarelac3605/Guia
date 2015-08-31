# Guia
Guia 3
#include <iostream> 
#include <string> 

using namespace std;
 
class base {
   private:
      string nom, dep, pos; 
      int sal;
   public:
      void imprime();
      void Guarda(string n2, string d2, string p2, int s2) {
         nom = n2;
         dep = d2;
         pos = p2;
         sal = s2;
         cout<<"Datos guardados exitosamente!" << endl;    
      }
};

void base::imprime() {
   cout << "Nombre: " << nom << endl;
   cout << "Departamento: " << dep << endl;
   cout << "Posicion: " << pos << endl;
   cout << "Salario: " << sal << endl;
}

int main() {
   base emp1;
   string nomb, depa, posi;
   int op, sala;
   
   
   do 
  { 
     cout << "1) Ingresar empleado " << endl;
     cout << "2) Leer empleado " << endl;
     cout << "3) Acerca de..." << endl;
     cout << "4) Salir " << endl;
     
     cout << "Por favor, seleccione una opcion: ";
     cin >> op;  
     
     if(op == 1) 
     {

        cout<<"ingrese nombre: "<<endl;
        cin>>nomb;
        cout<<"ingrese departamento: "<<endl;
        cin>>depa;
        cout<<"ingrese posicion: "<<endl;
        cin>>posi;
        cout<<"ingrese salario: "<<endl;
        cin>>sala;
        emp1.Guarda(nomb, depa, posi, sala);
     }
     else if(op == 2) 
     {
       emp1.imprime();
     }
     else if(op == 3) 
     {
        cout << "Programa realizado por:" << endl;
        cout << "David Varela Correa" << endl;
        cout << "UNIVERIDAD EAN" << endl;
     }
     else if(op == 4) 
     {
       cout << "Saliendo..." << endl;
     }
     else 
     {
       cout << "Opcion invalida, intente de nuevo... " << endl;
     }
  }
  while(op != 4); 
   
   return 0;
 
}
