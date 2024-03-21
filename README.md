# clase-2-optativa
--------Main----------(Clase)


package clase_2_java;

public class mail {

	public static void main(String[] args) {
		ManipularCSV vial = new ManipularCSV();
		vial.leerArchivo("C:\\Users\\estudiante\\Desktop\\clase 2 Optativa 1\\Vial.csv");
	}

}





-------ManipularCSV---------(Clase)

package clase_2_java;


import java.io.BufferedReader;
import java.io.FileReader;


public class ManipularCSV {
	
	
	private BufferedReader lector;
	private String linea;
	private String partes[] = null;
	
	
	public void leerArchivo(String NombreArchivo){
		try {
			lector = new BufferedReader(new FileReader(NombreArchivo));
			while((linea = lector.readLine()) != null) {
				partes = linea.split(",   ");
				imprimirLinea();
				System.out.println("-----------------------------");
				
			}
			lector.close();
			linea = null;
			partes = null;
			
				
		}catch (Exception e) {
			System.out.println("No funca esta mierdaaaa");
		}
	}
	
	public void imprimirLinea() {
		for(int i = 0; i < partes.length; i++) {
			System.out.println(partes[i]);
			
		}
	}
}
