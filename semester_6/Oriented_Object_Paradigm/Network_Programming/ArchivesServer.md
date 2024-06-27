Here is a example explained by me about a server that send's a file to every client that request it.
```Java
public class CServidorArchivo {

public final static int PUERTO = 13268; //puerto de conexión

public final static String ARCHIVO_A_ENVIAR = "/home/richy/ejemplo.sql"; //archivo a ser enviado

  

/**

* @param args the command line arguments

*/

public static void main(String[] args) throws IOException {

FileInputStream fis = null; // este objeto lee bytes, aqui se usa para leer el archivo

BufferedInputStream bis = null; // este objeto tambien lee bytes pero almacenando en un buffer temporal (lo cual lo hace mas eficiente)

OutputStream os = null; // se usa para enviar los bytes del archivo

ServerSocket skServidor = null; // se usa para recibir una conexion y enviar el archivo

Socket sk = null; // se crea un socketsillo para la conexion entre el server y cleiente

try {

skServidor = new ServerSocket(PUERTO); // se abre el server

while (true) {

System.out.println("Esperando conexión...");

try {

sk = skServidor.accept(); // se acepta una conexion al server

  

System.out.println("Conexión aceptada : " + sk);

  

// proceso para enviar el archivo

File archivo = new File (ARCHIVO_A_ENVIAR); // se crea un archivo local con el archivo que se va a enviar

byte [] ab = new byte [(int)archivo.length()]; //se crea un array de bytes

fis = new FileInputStream(archivo); // se crea un objeto para leer el archivo

bis = new BufferedInputStream(fis); // se crea un objeto para leer el archivo pero almacenando en un buffer temporal

bis.read(ab,0,ab.length); // se lee el archivo usando el buffer temporal

os = sk.getOutputStream(); // se obtiene el outputstream del socket (es decir el canal de salida de bytes)

  

System.out.println("Enviando " + ARCHIVO_A_ENVIAR + "(" + ab.length + " bytes)");

  

os.write(ab,0,ab.length); // se envian los bytes del archivo por el canal de salida

// os.flush();

System.out.println("Enviado.");

}

finally {

// cerrar todo el merequetengue

if (bis != null) bis.close();

if (os != null) os.close();

if (sk!=null) sk.close();

}

}

}

finally {

// cerrar el server

if (skServidor != null) skServidor.close();

}

}

}
```