package trabalho;

import edu.princeton.cs.algs4.*;
import java.util.*;

public class GrafoNaoDirecionado {

    private static final String NOVA_LINHA = System.lineSeparator();

    private final int numeroVertices;
    private int numeroArestas;
    private List<Integer>[] listasAdjacencia;

    // lê arquivo e retorna txt de graus
    public GrafoNaoDirecionado(Scanner entrada) {
        if (entrada == null)
            throw new IllegalArgumentException("Entrada nula");

        try {
            Map<Integer, Integer> mapaVertices = new HashMap<>();
            List<int[]> arestas = new ArrayList<>();

            // leitura linha por linha (dataset real)
            while (entrada.hasNextLine()) {
                String linha = entrada.nextLine().trim();

                // ignora comentários e linhas vazias
                if (linha.isEmpty() || linha.startsWith("#"))
                    continue;

                String[] partes = linha.split("\\s+");
                if (partes.length < 2) continue;

                int origemOriginal = Integer.parseInt(partes[0]);
                int destinoOriginal = Integer.parseInt(partes[1]);

                // mapeia IDs grandes para índices compactos
                mapaVertices.putIfAbsent(origemOriginal, mapaVertices.size());
                mapaVertices.putIfAbsent(destinoOriginal, mapaVertices.size());

                arestas.add(new int[]{origemOriginal, destinoOriginal});
            }

            // cria grafo
            this.numeroVertices = mapaVertices.size();
            this.numeroArestas = 0;

            listasAdjacencia = new ArrayList[numeroVertices];
            for (int v = 0; v < numeroVertices; v++) {
                listasAdjacencia[v] = new ArrayList<>();
            }

            // adiciona arestas já convertidas
            for (int[] e : arestas) {
                int v = mapaVertices.get(e[0]);
                int w = mapaVertices.get(e[1]);
                adicionarAresta(v, w);
            }

        } catch (Exception e) {
            throw new IllegalArgumentException("Formato de entrada inválido", e);
        }
    }

    // le o arquivo e retorna txt no modelo algs4
    public GrafoNaoDirecionado(In in) {
        if (in == null)
            throw new IllegalArgumentException("Entrada nula");

        try {
            Map<Integer, Integer> mapaVertices = new HashMap<>();
            List<int[]> arestas = new ArrayList<>();

            // leitura linha por linha (dataset real)
            while (in.hasNextLine()) {
                String linha = in.readLine().trim();

                // ignora comentários e linhas vazias
                if (linha.isEmpty() || linha.startsWith("#"))
                    continue;

                String[] partes = linha.split("\\s+");
                if (partes.length < 2) continue;

                int origemOriginal = Integer.parseInt(partes[0]);
                int destinoOriginal = Integer.parseInt(partes[1]);

                // mapeia IDs grandes para índices compactos
                mapaVertices.putIfAbsent(origemOriginal, mapaVertices.size());
                mapaVertices.putIfAbsent(destinoOriginal, mapaVertices.size());

                arestas.add(new int[]{origemOriginal, destinoOriginal});
            }

            // cria grafo
            this.numeroVertices = mapaVertices.size();
            this.numeroArestas = 0;

            listasAdjacencia = new ArrayList[numeroVertices];
            for (int v = 0; v < numeroVertices; v++) {
                listasAdjacencia[v] = new ArrayList<>();
            }

            // adiciona arestas já convertidas
            for (int[] e : arestas) {
                int v = mapaVertices.get(e[0]);
                int w = mapaVertices.get(e[1]);
                adicionarAresta(v, w);
            }

        } catch (Exception e) {
            throw new IllegalArgumentException("Formato de entrada inválido", e);
        }
    }

    public void printar(){
        In in = new In("Cit-HepTh.txt");
        Out out = new Out("algs4.txt");
        out.println(obterNumeroVertices() + "\n" + obterNumeroArestas());
        while(!in.isEmpty()){
            String linha = in.readLine().trim();

            if(linha.isEmpty() || linha.startsWith("#")){
                continue;
            }
            out.println(linha);
        }
        out.close();
    }

    // getters
    public int obterNumeroVertices() {
        return numeroVertices;
    }

    public int obterNumeroArestas() {
        return numeroArestas;
    }

    // valida vértice
    private void validarVertice(int vertice) {
        if (vertice < 0 || vertice >= numeroVertices)
            throw new IllegalArgumentException(
                    "Vértice " + vertice + " fora do intervalo 0 a " + (numeroVertices - 1));
    }

    // adiciona aresta
    public void adicionarAresta(int origem, int destino) {
        validarVertice(origem);
        validarVertice(destino);

        numeroArestas++;
        listasAdjacencia[origem].add(destino);
        listasAdjacencia[destino].add(origem);
    }

    // grau
    public int getGrau(int vertice) {
        validarVertice(vertice);
        return listasAdjacencia[vertice].size();
    }

    public void imprimirListaAdjacencia() {
        for (int v = 0; v < numeroVertices; v++) {
            System.out.print(v + ": ");
            for (int w : listasAdjacencia[v]) {
                System.out.print(w + " ");
            }
            System.out.println();
        }
    }
