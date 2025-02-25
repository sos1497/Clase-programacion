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
// See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, world");

var lista_clientes = new List<Clientes>();
lista_clientes.Add(new Clientes() {Id=1,Cedula="321",Nombre="Pedro" });
lista_clientes.Add(new Clientes() { Id = 2, Cedula = "485", Nombre = "Luis" });
lista_clientes.Add(new Clientes() { Id = 3, Cedula = "371", Nombre = "Ana" });

//foreach (var elemento in lista_clientes) Console.WriteLine(elemento.Nombre);

var cliente = lista_clientes.FirstOrDefault(x => x.Cedula == "321");
if (cliente != null)
    Console.WriteLine(cliente.Nombre);

public class Clientes
{
    public int Id { get; set; }
    public string? Cedula { get; set; }
    public string? Nombre { get; set; }
}
public class Productos
{
    public int Id { get; set; }
    public string? Codigo { get; set; }
    public string? Nombre { get; set; }
    public string? Tipo { get; set; }
    public string? Marca { get; set; }
    public double cantidad { get; set; }
}
public class Facturas
{
    public int id { get; set; }
    public string? Codigo { get; set; }
    public int Cliente { get; set; }
    public DateTime Fecha { get; set; }
    public double IVA { get; set; }
    public double Descuento { get; set; }
    public double Total { get; set; }
    public Clientes? _Cliente { get; set; }
    public List<Facturas_Productos>? Facturas_Productos { get; set; }
}
public class Facturas_Productos
{
    public int id { get; set; }
    public int Factura { get; set; }
    public int Producto { get; set; }
    public double Cantidad { get; set; }
    public double IVA { get; set; }
    public double Descuento { get; set; }
    public double SubTotal { get; set; }
    public Facturas? _Factura { get; set; }
    public Productos? _Producto { get; set; }
}
------------------------------------------------------------------------    
