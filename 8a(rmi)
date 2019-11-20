AddIntface.java

import java.rmi.*;
public interface AddServerIntf extends Remote {
  int add(int x, int y) throws RemoteException;
}

AddServerImpl.java

import java.rmi.*;
import java.rmi.server.*;
public class AddServerImpl extends UnicastRemoteObject implements
AddServerIntf{
  public AddServerImpl() throws RemoteException {}
  public int add(int x, int y) throws RemoteException {
  return x+y;
  }
}

AddServer.java

import java.rmi.*;
public class AddServer {
public static void main(String[] args) {
  try{
  AddServerImpl server = new AddServerImpl();
  Naming.rebind("registerme",server);
  System.out.println("Server is running..."); 
  }
   catch (Exception e) {
  System.out.println(e);
    }
  }  
}

AddClient.java

import java.rmi.*;
public class AddClient {  
   public static void main(String[] args) {
    try{
      AddServerIntf client = (AddServerIntf)Naming.lookup("registerme");
      System.out.println("First number is :" + args[0]);  
      int x = Integer.parseInt(args[0]);
      System.out.println("Second number is :" + args[1]);
      int y = Integer.parseInt(args[1]);
      System.out.println("Sum =" + client.add(x,y));  
      }
      catch (Exception e){
        System.out.println(e);
       }
    }
}
