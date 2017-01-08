# Java_session_Assignment4.4
//Constructor chaining

public class ConstructorChain{

  public static void main(String args[])
   {
    Derived sub = new Derived("Test"); 
    }
}

class Base{
    protected String name;
  
    public Base(){
        this(""); 
        System.out.println("Inside no argument constructor of Base class");
    }
  
    public Base(String name){
        this.name = name;
        System.out.println("One arg constructor of Base class");
    }
}

class Derived extends Base{
  
   public Derived(){
       System.out.println("Inside no argument constructor of Derived class");
   }
  
   public Derived(String name){
       super(name); //calling one argument constructor of super class
       System.out.println("Inside one arg constructor from Derived class");
   }
}
