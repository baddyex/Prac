# Prac

public class A {
    
    static int p;
    static int u;       

    int i;
    int j;
    
    
    static
    {
         u=99;                                           //yaha pe sirf static initialize krskte
         p= 88888;
                System.out.println ("SIB only once");    //no obj create req , runs only oncw , juss write static over it
                System.out.println (u);
               System.out.println (p);
               
               // System.out.println (i);   // erroe ayega coz i NS

    }
    
    
    static
    {
                System.out.println ("SIB dusra");

    }
    
    
    
    
   //NS IIB
    {
        p=88;                                        //yaha pe IIB- static NC dono new initialize krskte
        i= 10;
        j= 48;
        System.out.println ("IIB pehla");
                System.out.println (i);                 // obj create , runs multiple as per obj created
                
                System.out.println (p);     //static hai obj creat not req
                System.out.println (u);

    }
    
    {
                System.out.println ("IIB dusra");

        
    }
   



    //Cons 
    A(){
        
       
        System.out.println ("cons");
                System.out.println (i);        //cons NS b dega obj bana k
                System.out.println (p);        //cons static b dega


    }
    
    
    
    public static void main(String args[]) {
        
                System.out.println ("start main");

   
    A a1 = new A();
    A a2 = new A();

    System.out.println ("-------------------------------");

    System.out.println (a1.i);
    System.out.println (a1.j);
 
 
    System.out.println (a2.i);
    System.out.println (a2.j);
        
    System.out.println ("--------------------------------");

   
   
    System.out.println("end main");
   
   
   
    }
    
    
  
}



SIB only once
99
88888
SIB dusra
start main
IIB pehla
10
88
99
IIB dusra
cons
10
88
IIB pehla
10
88
99
IIB dusra
cons
10
88
-------------------------------
10
48
10
48
--------------------------------
end main

