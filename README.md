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
// See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, world");
var Lista_estudiantes=new List<Estudiantes>();
Lista_estudiantes.Add(new Estudiantes() { Id = 1, Carnet = "101", Nombre = "Sofia", Fecha = DateTime.Now, Carrera = "Desarrollo" });
Lista_estudiantes.Add(new Estudiantes() { Id = 2, Carnet = "102", Nombre = "Pedro", Fecha = DateTime.Now, Carrera = "Ingenieria" });
Lista_estudiantes.Add(new Estudiantes() { Id = 3, Carnet = "103", Nombre = "Marcela", Fecha = DateTime.Now, Carrera = "Contabilidad" });
var Lista_profesores=new List<Profesores>();
Lista_profesores.Add(new Profesores() { Id = 1, Codigo = "1020", Nombre = "Juan", Correo = "abc@gmail.com", Numcontrato = "123" });
Lista_profesores.Add(new Profesores() { Id = 2, Codigo = "1021", Nombre = "Carlos", Correo = "def@gmail.com", Numcontrato = "124" });
Lista_profesores.Add(new Profesores() { Id = 3, Codigo = "1022", Nombre = "Ana", Correo = "bit@gmail.com", Numcontrato = "125" });
Lista_profesores.Add(new Profesores() { Id = 4, Codigo = "1023", Nombre = "Rodolfo", Correo = "got@gmail.com", Numcontrato = "126" });
var Lista_profesores_estudiantes = new List<ProfesoresEstudiantes>();
Lista_profesores_estudiantes.Add(new ProfesoresEstudiantes() { Id = 1, Profesor = 1, Estudiante = 1 });
Lista_profesores_estudiantes.Add(new ProfesoresEstudiantes() { Id = 2, Profesor = 1, Estudiante = 2, _Profesor = Lista_profesores[0], _Estudiante= Lista_estudiantes[1] });
Lista_profesores_estudiantes.Add(new ProfesoresEstudiantes() { Id = 3, Profesor = 3, Estudiante = 2, _Profesor = Lista_profesores.FirstOrDefault(x => x.Codigo=="1022"), _Estudiante = Lista_estudiantes.FirstOrDefault(x => x.Carnet=="102") });
Lista_profesores_estudiantes.Add(new ProfesoresEstudiantes() { Id = 4, Profesor = 3, Estudiante = 3 });
Lista_profesores_estudiantes.Add(new ProfesoresEstudiantes() { Id = 5, Profesor = 2, Estudiante = 1 });
Lista_profesores_estudiantes.Add(new ProfesoresEstudiantes() { Id = 6, Profesor = 4, Estudiante = 3 });
foreach (var elemento in Lista_profesores_estudiantes) Console.WriteLine(elemento.Id + elemento.Profesor  + elemento.Estudiante);


public class Estudiantes
{
    public int Id { get; set; }
    public string? Carnet { get; set; }
    public string? Nombre { get; set; }
    public DateTime? Fecha { get; set; }
    public string? Carrera { get; set; }
    public List<ProfesoresEstudiantes>? ProfesoresEstudiantes { get; set; }
}
public class Profesores
{
    public int Id { get; set; }
    public string? Codigo { get; set; }
    public string? Nombre { get; set; }
    public string? Correo { get; set; }
    public string? Numcontrato { get; set; }
    public List<ProfesoresEstudiantes>? ProfesoresEstudiantes { get; set; }
}
public class ProfesoresEstudiantes
{
    public int Id { get; set; }
    public int Profesor { get; set; }
    public int Estudiante { get; set; }
    public Profesores? _Profesor { get; set; }
    public Estudiantes? _Estudiante { get; set; }
}
// Herencia e interfaces
public class Abuelos { };
public class Padres : Abuelos { };
public class Hijos : Padres { };
