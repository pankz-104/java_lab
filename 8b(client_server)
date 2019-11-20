//  client.java


import java.net.*;
import java.io.*;

public class Client8b {
	public static void main(String [] args)
	{
		Socket Client = null;
		BufferedReader br = null;
		try
		{
			System.out.println(args[0]+" "+args[1]);
			Client = new Socket(args[0],Integer.parseInt(args[1])); 
		}
		catch(Exception e)
		{}
		DataInputStream input = null;
		PrintStream output = null;
		try {
			input = new DataInputStream(Client.getInputStream());
			output = new PrintStream(Client.getOutputStream());
			br = new BufferedReader(new InputStreamReader(System.in));
			String str = input.readLine();
			System.out.println(str);
			String filename = br.readLine();
			if(filename != null)
			{
				output.println();
			}
			String data;
			while((data = input.readLine())!= null)
			{
				System.out.println(data);
			}
			Client.close();
		}
		catch(Exception e) {
			System.out.println(e);
		}
		
	}
}


// server.java

import java.net.*;
import java.io.*;
public class Server8b {
	public static void main(String args[])
	{
		ServerSocket Server = null;
		try {
			Server = new ServerSocket(Integer.parseInt(args[0]));
		}
		catch(Exception e) {}
		while (true)
		{
			Socket Client = null;
			PrintStream Output = null;
			DataInputStream input = null;
			try {
				Client = Server.accept();
			}
			catch(Exception e)
			{
				System.out.println(e);
			}
			try {
				Output = new PrintStream(Client.getOutputStream());
				input = new DataInputStream(Client.getInputStream());
			}
			catch(Exception e)
			{
				System.out.println(e);
			}
			Output.println("enter file name: > ");
			try {
				String filename = input.readLine();
				System.out.println("client requested file:"+filename);
				try {
					File f = new File(filename);
					BufferedReader br = new BufferedReader(new FileReader(f));
					String data;
					while((data = br.readLine())!=null)
					{
						Output.println(data);
					}
				}
				catch(FileNotFoundException e)
				{
					Output.println("file not found");
				}
				Client.close();
			}
			catch(Exception e)
			{
				System.out.println(e);
			}
		}
	}
}
