package leertxt;

import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;

public class dos {
   
    dos()throws IOException {
    
    String frase="El nino tiene la pelota";
    String frase2[]=frase.split(" ");
       
    String dir="C:\\Users\\Yael Leon\\Documents\\yael\\hola.txt";
    FileReader f= new FileReader(dir);
    BufferedReader br= new BufferedReader(f);
    
    String mala=br.readLine();
    br.close();
    String[] malo=mala.split(" ");
    //System.out.println(mala);
    String auxiliar[]= new String[frase2.length]; 
    
        for (int i = 0; i < malo.length; i++) {
            for (int j = 0; j<malo.length; j++) {
                if (malo[i].equals(frase2[j])) {               
                auxiliar[j]=malo[i];                
                }
            }
        }
        String buena=" ";
        for (int i = 0; i < auxiliar.length; i++) {
            buena+=auxiliar[i]+" ";
        }
         System.out.println(buena);
    }
}
