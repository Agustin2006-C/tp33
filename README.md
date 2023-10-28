#ifndef Paciente_H
#define	Paciente_H
#include <string>
#include <iostream>
 
using namespace std;
 
class CPaciente {
public:
    CPaciente (string nombre, string dire, int telefono, bool OS, bool alergia, int ultimavisita);
  CPaciente();
   
    string getNombre();
    string getdire();
    int gettelefono();
    bool getOS();
	bool getalergia();
	int getultimavisita();    
private:
    string nombre;
    string dire;
    int telefono;
    bool OS;
    bool alergia;
    int ultimavisita;
};
 
 
 
 
CPaciente::CPaciente (string n, string d,int t, bool OS, bool a, int uv){
 
    nombre = n;
    dire= d;
    telefono = t;
    OS=OS;
    alergia=a;
    ultimavisita=uv;
 
}
 
 
string CPaciente::getNombre(){
 
    return nombre;
 
}
 
 
CPaciente::CPaciente (){
 
}

  
string CPaciente::getdire(){
 
    return dire;
 
}
 
int CPaciente::gettelefono(){
 
    return telefono;
 
}

bool CPaciente::getOS(){
	return OS;
}

bool CPaciente::getalergia(){
	return alergia;
}

int CPaciente::getultimavisita(){
	return ultimavisita;
}
	

#endif	/* CPaciente_H */


#include <cstdlib>
#include <iostream>
#include "Paciente.h" 
 
using namespace std;
 
void desplegarDatosOS(CPaciente *arreglo){
 
    cout <<"\n\nDesplegando datos de las OS\n\n";
 
    for(int i=0; i<6; i++){
  			if(arreglo[i].getOS()==true)
  			{
			  
        cout <<"\nNombre: " << arreglo[i].getNombre();
        cout <<"\ndire: " << arreglo[i].getdire();
        cout <<"\ntelefono: " << arreglo[i].gettelefono();
        cout <<"\nOS: " << arreglo[i].getOS();
		cout <<"\nalergia: " << arreglo[i].getalergia();
		cout <<"\nultimavisita: " << arreglo[i].getultimavisita();
		
		cout <<"\n";
 	        }
    }
 
}
 
int main(int argc, char** argv) {
 
    cout <<"Creando un arreglo de OS";
 int e=0;
    CPaciente *OS = new CPaciente[6];
 
    paciente[0] = CPaciente("Rodrigo","vertiz 380","123456", true,true,2019);
    paciente[1] = CPaciente("Francisco","santa fe 340","167890",true,true,198);
    paciente[2] = CPaciente("Samuel","juan b justo 3400","567421",true,true,2367);
    paciente[3] = CPaciente("Damian","bosch 234","2435678",false,false,2467);
    paciente[4] = CPaciente("Agustin","edison 354","244567",false,true,2467);
	paciente[5] = CPaciente("Mirko","san juan 567","123456",true,false,2456);
	 
 
 	
    desplegarDatosOS(pacientes);
 
  for(int i=0; i<6; i++){
 	
 	e += paciente[i].getOS(); 	
 	
}
cout<<"OS:"<<e<<endl;



    delete []pacientes;
 
    return 0;
}
 
