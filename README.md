# Exc-
Esempio c++
#include<iostream>
#include<string>
#include<stdlib.h>

using namespace std;
 int menu();
 int inserisci();
 int sposta();

string slot1,slot2,slot3,slot4;
         
int main()
{


  cout<<"Temporanea Gestione"<<endl;
slot1="Vuoto";
         slot2="Vuoto";
	 slot3="Vuoto";
 	 slot4="Vuoto";
  
         
  menu();

}
int menu()
{      
     system("clear");
     string comando;
     cout<<"|Slots Disponibili |"<<endl;
     cout<<"|"<<"1"<<"|"<<slot1<<"|"<<endl;
     cout<<"|"<<"2"<<"|"<<slot2<<"|"<<endl;
     cout<<"|"<<"3"<<"|"<<slot3<<"|"<<endl;
     cout<<"|"<<"4"<<"|"<<slot4<<"|"<<endl;
     cout<<"|Comandi disponibili|"<<"|Inserisci|"<<"|Sposta|"<<endl;
     
      do 
      {
        cin>>comando;
     if (comando=="inserisci")
    {
       inserisci();
     }
     if (comando=="sposta")
     {
       sposta();
      }
      else 
      { 
        cout<<"Comando errato,riprova"<<endl; 
      } 
      
      }while(comando!="inserisci" || comando!= "sposta") ;
       
}
int inserisci()
{    
     system("clear");
     int ns;     //Numero della slot 
     string  n;  // Testo da inserire nella slot 
    
      
     cout<<"\n Inserire il nome dell oggetto da inserire nella slot ";
     cin>>n;
     cout<<"\n Inserisci il numero della slot che deve contenere questo oggetto";
     do{
      cout<<"(1,2,3,4)"<<endl;
     cin>>ns;
     }while(ns>4);
     switch (ns)
     {
       case 1:
          
          slot1=n;
          cout<<"Inserito correttamente"<<slot1<<endl;
          menu();
          break;
       case 2:
          
          slot2=n;
 	  cout<<"Inserito correttamente"<<slot2<<endl;
          menu();
          break;
       case 3:
 	  
          slot3=n;
	  cout<<"Inserito correttamente"<<slot3<<endl;
          menu();
          break;
       case 4:
          
          slot4=n;
          cout<<"Inserito correttamente"<<slot4<<endl;
          menu();
          break;

     } 
      
     
     
     
     
}
int sposta() 
{   
    system("clear");
    int ns,sn;
    string temp; 
    temp="";
    cout<<"Inserisci il numero della slot da dove vuoi prelevare l'oggetto "<<endl;
    do{
      cout<<"(1,2,3,4)"<<endl;
     cin>>ns;
     }while(ns>4);
    cout<<"Inserisci il numero della slot dove vuoi riposizionarlo"<<endl;
    cin>>sn;
    switch (ns)
     {
       case 1 : 

          temp=slot1; 
          slot1="Vuoto";
          break;
       case 2 : 
          temp=slot2; 
          slot2="Vuoto";
          break;
       case 3 : 
          temp=slot3; 
          slot3="Vuoto";
          break;
       case 4 : 
          temp=slot4; 
          slot4="Vuoto";
          break;
     }
     switch (sn)
     {
       case 1 : 
          slot1=temp; 
          break;
       case 2 : 
          slot2=temp; 
          break;
       case 3 : 
          slot3=temp; 
          break;
       case 4 : 
          slot4=temp; 
          break;
     }
     cout<<"Operazione eseguita correttamente"<<endl;
     
     menu();



}
