//callback.java

package callback;
public interface Callback {
void Callback(int param);
}

//client.java

package callback;
public class Client implements Callback{
public void Callback(int param) {
System.out.println("Callback called with "+param);
}
}

//test.java

package callback;
public class Test {
public static void main(String[] args) {
Callback c = new Client();
c.Callback(42);
}
}

