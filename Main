package trabalho;

import edu.princeton.cs.algs4.*;
import java.io.File;
import java.io.PrintWriter;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        In in = new In("Cit-HepTh.txt");
        GrafoNaoDirecionado grafoo = new GrafoNaoDirecionado(in);

        //19769
        grafoo.imprimirListaAdjacencia();
        grafoo.printar();


        try (
                Scanner entrada = new Scanner(new File("Cit-HepTh.txt"));
                PrintWriter writer = new PrintWriter("graus.txt")
        ) {

            GrafoNaoDirecionado grafo = new GrafoNaoDirecionado(entrada);

            System.out.println(grafo);

            int somaGraus = 0;

            // escreve graus no arquivo (formato simples: vertice grau)
            for (int v = 0; v < grafo.obterNumeroVertices(); v++) {
                int grau = grafo.getGrau(v);
                writer.printf("%d %d%n", v, grau); // <-- formato ajustado
                somaGraus += grau;
            }

            System.out.println("Arquivo graus.txt gerado com sucesso!");

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
