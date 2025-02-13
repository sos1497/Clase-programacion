# Clase-programacion
primera actualizacion
segundo cambio
cuarto cambio
hola
cambio tres
cuarto cambio 
suavemente 
2
oll
------------------------------------------------
// See https://aka.ms/new-console-template for more information
//TiposPersonajes tipo= new TiposPersonajes();
//var tipo= new TiposPersonajes(1,"Goku");
var tipo2= new TiposPersonajes(){id=2,name="Vegetta"};
Console.WriteLine(tipo2.name);
var pers= new Personajes(){id=1234,name="Gato",fecha=DateTime.Now,tamaño=172,vivo=true,tipo=new TiposPersonajes(3123,"pablo")};

public class TiposPersonajes
{
    public int id;
    public string? name=null;
    public TiposPersonajes(){

    }
    public TiposPersonajes(int id, string? name){
        this.id=id;
        this.name=name;
        Console.WriteLine("nombre: "+name);
        Console.WriteLine("identificacion: "+id);
    }

}
public class Personajes
{
    public int id;
    public string? name=null;
    public DateTime? fecha=null;
    public double tamaño;
    public bool vivo;
    
    public TiposPersonajes? tipo;
}
--------------------------------------------------
