# classupeu223
LP121
 
  import java.util.Scanner;

public class Archi01 {
  public static int [ ] llenarArreglo ( int elementos ) {
    int i; int [ ] v; 
    v = new int [ elementos ];
    Scanner sc = new Scanner ( System.in );

    for ( i = 0; i < elementos; i++ ) {
      System.out.print ( "v [ " + i + " ] = " );
      v [ i ] = sc.nextInt ( ); 
    }

    return v;
  }
  public static double promedio ( int [ ] v ) {
    double prom = 0.0;
    for ( int i = 0; i < v.length; i++ )
      prom += v[i];

    return prom / ( double ) v.length;  
  }
  public static int [ ] burbuja ( int [ ] v, int ord ) {
    int i, j, n = v.length, aux = 0;
    
    for ( i = 0; i < n - 1; i++ )
      for ( j = i + 1; j < n; j++ )
        if ( ord == 0 )
          if ( v [ i ] > v [ j ] ) {
            aux = v [ j ];
            v [ j ] = v [ i ];
            v [ i ] = aux;
          }
        else if ( ord == 1 )
          if ( v [ i ] < v [ j ] ) {
            aux = v [ i ];
            v [ i ] = v [ j ];
            v [ j ] = aux;
          }

    return v;
  }
    public static void reportaVector ( int [ ] v ) {
    for ( int i = 0; i < v.length; i++ )
      System.out.print ( v [ i ] + " " );
    System.out.println ( "" );
  }
  public static void main ( String [ ] args ) {
    int n; int [] v;
    double media;
    Scanner sc = new Scanner ( System.in );
    System.out.println ( "Ingrese la cantidad de numeros : ");
    n = sc.nextInt ( );

    v = llenarArreglo ( n );
    media = promedio ( v );
        
    System.out.println ( " Media v: " + media);
    
    reportaVector ( v );
  }
}
