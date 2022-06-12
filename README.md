# Exercicio-5-em-Java

# Exercicio replicado do livro Tutorial de programação em Java e Orientação em Objetos 

# Classe trava:

# O estado da trava é representado no atributo public boolean travado; e pode ser obtido através
# de uma chamada ao método estado(). Este exemplo é bastante simples e não tem a pretensão de ser
# uma implementação completa de uma classe que modele uma trava que possa ser usada para evitar o
# acesso a um arquivo, por exemplo.

public class Trava {
public String quem; //quem travou ou destravou por ultimo
public boolean travado;
public void trave(String q) 
{
this.travado = true;
this.quem = q;
}
public void destrave(String q)
{
this.travado = false;
this.quem = q;
}
public boolean estado()
//estado(true/false) do objeto
{
return travado;
}
}
//Classe principal, Arquivo Principal.Java
public class Principal {
 public static void main(String args[]) {
 Trava umatrava; 
 umatrava=new Trava();
 umatrava.trave("ProgramaPrincipal");
 System.out.println(umatrava.estado());
 umatrava.destrave("ProgramaPrincipal");
 System.out.println(umatrava.estado());
 
 }
}

//COMENTARIOS
//A classe trava é demasiadamente simples, mas se não o fosse não estaria na parte introdutória
//deste tutorial. Esta classe acaba tendo a funcionalidade de uma variável booleana e o custo de um
//objeto, mas neste ponto cabe a você melhorar este modelo para representar uma trava de arquivo
//(armazena o nome e “path” deste) ou uma trava de um objeto, evitando que este seja alterado.
