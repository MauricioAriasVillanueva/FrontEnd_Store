<!-- Header Principal -->
<header class="bg-gradient-to-r from-indigo-700 via-purple-700 to-pink-600 text-white shadow-lg p-6 no-print">
    <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
        <div>
            <span class="bg-white/20 text-xs px-3 py-1 rounded-full uppercase tracking-wider font-semibold">OdinsoftNorte S.A.C.</span>
            <h1 class="text-3xl font-extrabold mt-1">Canvas Interactivo de Programación Funcional</h1>
            <p class="text-indigo-100 text-sm mt-1">Aprende Java Funcional, Streams, Lambdas y Records con ejemplos visuales</p>
        </div>
        <button onclick="window.print()" class="bg-emerald-500 hover:bg-emerald-600 text-white font-bold py-2.5 px-5 rounded-lg shadow-md transition flex items-center gap-2">
            <i class="fa-solid fa-print"></i> Guardar / Imprimir PDF
        </button>
    </div>
</header>

<main class="max-w-7xl mx-auto p-4 md:p-6 space-y-8">

    <!-- Navegación por Secciones (Tabs Visuales) -->
    <nav class="flex flex-wrap gap-2 border-b border-slate-300 pb-3 no-print">
        <button onclick="showTab('glosario')" id="btn-glosario" class="tab-btn active px-4 py-2 rounded-lg font-semibold bg-indigo-600 text-white flex items-center gap-2">
            <i class="fa-solid fa-book-open"></i> 1. Glosario y Analogías
        </button>
        <button onclick="showTab('stream-flow')" id="btn-stream-flow" class="tab-btn px-4 py-2 rounded-lg font-semibold bg-white text-slate-700 hover:bg-slate-200 flex items-center gap-2">
            <i class="fa-solid fa-diagram-project"></i> 2. Flujo de Streams
        </button>
        <button onclick="showTab('codigo')" id="btn-codigo" class="tab-btn px-4 py-2 rounded-lg font-semibold bg-white text-slate-700 hover:bg-slate-200 flex items-center gap-2">
            <i class="fa-solid fa-code"></i> 3. Código por Paquetes
        </button>
        <button onclick="showTab('simulador')" id="btn-simulador" class="tab-btn px-4 py-2 rounded-lg font-semibold bg-white text-slate-700 hover:bg-slate-200 flex items-center gap-2">
            <i class="fa-solid fa-vial-circle-check"></i> 4. Simulador Interactivo
        </button>
    </nav>

    <!-- SECCIÓN 1: GLOSARIO DE CONCEPTOS Y ANALOGÍAS -->
    <section id="sec-glosario" class="space-y-6">
        <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200">
            <h2 class="text-2xl font-bold text-slate-800 border-b pb-3 flex items-center gap-3">
                <span class="bg-indigo-100 text-indigo-700 w-10 h-10 rounded-full flex items-center justify-center text-lg"><i class="fa-solid fa-lightbulb"></i></span>
                Glosario Ilustrado: Conceptos Clave en Palabras Simples
            </h2>
            <p class="text-slate-600 mt-2">Pasa el cursor o revisa cada tarjeta para entender los conceptos difíciles explicados con situaciones de la vida real.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-6">
                
                <!-- Card 1: extends -->
                <div class="bg-amber-50 border-l-4 border-amber-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-amber-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-sitemap text-xl"></i> extends
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-amber-900">Significado:</strong> Herencia ("Es un tipo de..."). Hereda las capacidades de otra clase.</p>
                    <div class="bg-white p-3 rounded-lg border border-amber-200 text-xs text-amber-950">
                        <strong> Analogía:</strong> Un <code>Perro</code> <strong>extends</strong> <code>Animal</code>. El perro hereda automáticamente la capacidad de comer y respirar de la clase Animal.
                    </div>
                </div>

                <!-- Card 2: super() -->
                <div class="bg-orange-50 border-l-4 border-orange-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-orange-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-phone-volume text-xl"></i> super()
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-orange-900">Significado:</strong> Llamada directa a la clase "padre" para que ella haga el trabajo pesado.</p>
                    <div class="bg-white p-3 rounded-lg border border-orange-200 text-xs text-orange-950">
                        <strong> Analogía:</strong> Si no sabes reparar un auto, usas <code>super()</code> para llamar a tu papá para que guarde el mensaje del problema por ti.
                    </div>
                </div>

                <!-- Card 3: record -->
                <div class="bg-emerald-50 border-l-4 border-emerald-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-emerald-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-box-archive text-xl"></i> record
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-emerald-900">Significado:</strong> Clase inmutable (sus datos no cambian una vez creada). Ahorra código de getters/setters.</p>
                    <div class="bg-white p-3 rounded-lg border border-emerald-200 text-xs text-emerald-950">
                        <strong> Analogía:</strong> Una fotografía impresa. Una vez tomada, no puedes mover a las personas dentro de la foto.
                    </div>
                </div>

                <!-- Card 4: .stream() -->
                <div class="bg-cyan-50 border-l-4 border-cyan-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-cyan-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-gears text-xl"></i> .stream()
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-cyan-900">Significado:</strong> Convierte una lista en una "cinta transportadora" de datos para procesarlos uno a uno.</p>
                    <div class="bg-white p-3 rounded-lg border border-cyan-200 text-xs text-cyan-950">
                        <strong> Analogía:</strong> La cinta de revisión del aeropuerto. Las maletas van pasando en fila por el escáner.
                    </div>
                </div>

                <!-- Card 5: .filter() -->
                <div class="bg-blue-50 border-l-4 border-blue-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-blue-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-filter text-xl"></i> .filter()
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-blue-900">Significado:</strong> Un colador. Solo deja pasar los elementos que cumplen una condición verdadera.</p>
                    <div class="bg-white p-3 rounded-lg border border-blue-200 text-xs text-blue-950">
                        <strong> Analogía:</strong> El filtro de seguridad de una discoteca que dice: "Solo entran mayores a 18 años".
                    </div>
                </div>

                <!-- Card 6: .map() -->
                <div class="bg-indigo-50 border-l-4 border-indigo-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-indigo-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-wand-magic-sparkles text-xl"></i> .map()
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-indigo-900">Significado:</strong> Transformador. Toma un objeto de entrada y lo convierte en otro distinto.</p>
                    <div class="bg-white p-3 rounded-lg border border-indigo-200 text-xs text-indigo-950">
                        <strong> Analogía:</strong> Una fábrica de exprimido: entra una naranja entera y sale un vaso de jugo.
                    </div>
                </div>

                <!-- Card 7: .reduce() -->
                <div class="bg-purple-50 border-l-4 border-purple-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-purple-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-calculator text-xl"></i> .reduce()
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-purple-900">Significado:</strong> Acumulador. Junta todos los elementos y los convierte en un solo valor.</p>
                    <div class="bg-white p-3 rounded-lg border border-purple-200 text-xs text-purple-950">
                        <strong> Analogía:</strong> Una alcancía donde echas monedas y al final obtienes un único valor total.
                    </div>
                </div>

                <!-- Card 8: groupingBy -->
                <div class="bg-pink-50 border-l-4 border-pink-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-pink-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-folder-tree text-xl"></i> groupingBy
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-pink-900">Significado:</strong> Clasificador. Agrupa los elementos según una categoría común.</p>
                    <div class="bg-white p-3 rounded-lg border border-pink-200 text-xs text-pink-950">
                        <strong> Analogía:</strong> Separar la ropa lavada por colores: un grupo para ropa blanca y otro para ropa oscura.
                    </div>
                </div>

                <!-- Card 9: Optional<T> -->
                <div class="bg-rose-50 border-l-4 border-rose-500 p-5 rounded-xl shadow-sm hover:shadow-md transition">
                    <div class="flex items-center gap-3 text-rose-800 font-bold text-lg mb-2">
                        <i class="fa-solid fa-gift text-xl"></i> Optional&lt;T&gt;
                    </div>
                    <p class="text-sm text-slate-700 mb-3"><strong class="text-rose-900">Significado:</strong> Caja de seguridad que puede o no contener un valor, evitando errores nulos.</p>
                    <div class="bg-white p-3 rounded-lg border border-rose-200 text-xs text-rose-950">
                        <strong> Analogía:</strong> Una caja de regalo transparente: si no hay nada dentro, simplemente está vacía, no explota.
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECCIÓN 2: DIAGRAMA DE FLUJO DE STREAMS -->
    <section id="sec-stream-flow" class="space-y-6 hidden">
        <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200">
            <h2 class="text-2xl font-bold text-slate-800 border-b pb-3 flex items-center gap-3">
                <span class="bg-cyan-100 text-cyan-700 w-10 h-10 rounded-full flex items-center justify-center text-lg"><i class="fa-solid fa-diagram-next"></i></span>
                Pipeline de Streams: La Cinta Transportadora de Datos
            </h2>
            <p class="text-slate-600 mt-2">Así viajan y se transforman los pedidos dentro del método <code>calcularTotalFacturado(...)</code>:</p>

            <!-- Flujo Visual -->
            <div class="mt-8 space-y-4">
                
                <!-- Paso 1 -->
                <div class="flex flex-col md:flex-row items-center gap-4 bg-slate-50 p-4 rounded-xl border border-slate-200">
                    <div class="bg-slate-700 text-white font-bold w-12 h-12 rounded-full flex items-center justify-center shrink-0">1</div>
                    <div class="flex-1">
                        <h3 class="font-bold text-slate-800">Origen: Colección Original</h3>
                        <p class="text-xs text-slate-600">Se tiene una lista con $n$ pedidos ingresados desde el formulario.</p>
                    </div>
                    <div class="bg-slate-200 px-3 py-1 rounded text-xs font-mono">List&lt;Pedido&gt;</div>
                </div>

                <div class="text-center text-indigo-500 text-xl"><i class="fa-solid fa-arrow-down"></i></div>

                <!-- Paso 2 -->
                <div class="flex flex-col md:flex-row items-center gap-4 bg-cyan-50 p-4 rounded-xl border border-cyan-200">
                    <div class="bg-cyan-600 text-white font-bold w-12 h-12 rounded-full flex items-center justify-center shrink-0">2</div>
                    <div class="flex-1">
                        <h3 class="font-bold text-cyan-900">.stream()</h3>
                        <p class="text-xs text-cyan-700">Abre la cinta transportadora. Los pedidos avanzan en secuencia sin modificar la lista original.</p>
                    </div>
                    <div class="bg-cyan-200 text-cyan-900 px-3 py-1 rounded text-xs font-mono">Stream&lt;Pedido&gt;</div>
                </div>

                <div class="text-center text-cyan-500 text-xl"><i class="fa-solid fa-arrow-down"></i></div>

                <!-- Paso 3 -->
                <div class="flex flex-col md:flex-row items-center gap-4 bg-blue-50 p-4 rounded-xl border border-blue-200">
                    <div class="bg-blue-600 text-white font-bold w-12 h-12 rounded-full flex items-center justify-center shrink-0">3</div>
                    <div class="flex-1">
                        <h3 class="font-bold text-blue-900">.filter(p -&gt; p.cantidad &gt; 0)</h3>
                        <p class="text-xs text-blue-700">El colador descarta los pedidos erróneos (cantidad &lt;= 0 o precio &lt;= 0) enviándolos a rechazos.</p>
                    </div>
                    <div class="bg-blue-200 text-blue-900 px-3 py-1 rounded text-xs font-mono">Solo Pedidos Válidos</div>
                </div>

                <div class="text-center text-blue-500 text-xl"><i class="fa-solid fa-arrow-down"></i></div>

                <!-- Paso 4 -->
                <div class="flex flex-col md:flex-row items-center gap-4 bg-indigo-50 p-4 rounded-xl border border-indigo-200">
                    <div class="bg-indigo-600 text-white font-bold w-12 h-12 rounded-full flex items-center justify-center shrink-0">4</div>
                    <div class="flex-1">
                        <h3 class="font-bold text-indigo-900">.map(p -&gt; calcularMontoConDescuento(p))</h3>
                        <p class="text-xs text-indigo-700">La fábrica transformadora convierte cada objeto Pedido en un número decimal con descuento aplicado (10%, 5% u 0%).</p>
                    </div>
                    <div class="bg-indigo-200 text-indigo-900 px-3 py-1 rounded text-xs font-mono">Stream&lt;Double&gt;</div>
                </div>

                <div class="text-center text-indigo-500 text-xl"><i class="fa-solid fa-arrow-down"></i></div>

                <!-- Paso 5 -->
                <div class="flex flex-col md:flex-row items-center gap-4 bg-purple-50 p-4 rounded-xl border border-purple-200">
                    <div class="bg-purple-600 text-white font-bold w-12 h-12 rounded-full flex items-center justify-center shrink-0">5</div>
                    <div class="flex-1">
                        <h3 class="font-bold text-purple-900">.reduce(0.0, Double::sum)</h3>
                        <p class="text-xs text-purple-700">La alcancía suma todos los montos individuales comenzando en 0.0 hasta obtener la facturación total.</p>
                    </div>
                    <div class="bg-purple-200 text-purple-900 px-3 py-1 rounded text-xs font-mono">double totalFacturado</div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECCIÓN 3: CÓDIGO FUENTE POR PAQUETES -->
    <section id="sec-codigo" class="space-y-6 hidden">
        <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200">
            <h2 class="text-2xl font-bold text-slate-800 border-b pb-3 flex items-center gap-3">
                <span class="bg-emerald-100 text-emerald-700 w-10 h-10 rounded-full flex items-center justify-center text-lg"><i class="fa-solid fa-code"></i></span>
                Código Fuente Organizado por Archivos
            </h2>

            <div class="flex flex-wrap gap-2 my-4 no-print">
                <button onclick="showCode('excepcion')" id="code-btn-excepcion" class="code-tab-btn active text-xs font-bold px-3 py-1.5 rounded-lg bg-slate-800 text-white">PedidoInvalidoException.java</button>
                <button onclick="showCode('pedido')" id="code-btn-pedido" class="code-tab-btn text-xs font-bold px-3 py-1.5 rounded-lg bg-slate-200 text-slate-700 hover:bg-slate-300">Pedido.java (Record)</button>
                <button onclick="showCode('servicio')" id="code-btn-servicio" class="code-tab-btn text-xs font-bold px-3 py-1.5 rounded-lg bg-slate-200 text-slate-700 hover:bg-slate-300">ProcesadorServicio.java</button>
                <button onclick="showCode('gui')" id="code-btn-gui" class="code-tab-btn text-xs font-bold px-3 py-1.5 rounded-lg bg-slate-200 text-slate-700 hover:bg-slate-300">FormularioApp.java (GUI)</button>
            </div>

            <!-- Code 1: Excepcion -->
            <div id="code-block-excepcion" class="code-container">
                <div class="text-xs text-slate-500 mb-1 font-mono">Paquete: com.odinsoft.modelo</div>
                <pre class="code-block p-4 rounded-xl text-xs overflow-x-auto"><code>package com.odinsoft.modelo;


// Hereda de Exception para darnos control sobre los errores de negocio
public class PedidoInvalidoException extends Exception {

// Recibe el mensaje específico de la falla y se lo pasa a la clase padre (Exception)
public PedidoInvalidoException(String mensaje) {
    super(mensaje);
}


}


            <!-- Code 2: Pedido Record -->
            <div id="code-block-pedido" class="code-container hidden">
                <div class="text-xs text-slate-500 mb-1 font-mono">Paquete: com.odinsoft.modelo</div>
                <pre class="code-block p-4 rounded-xl text-xs overflow-x-auto"><code>package com.odinsoft.modelo;


// El 'record' define los atributos inmutables directamente en la firma
public record Pedido(
String codigoCliente,
String producto,
int cantidad,
double precioUnitario,
String region
) {
// Método de validación que lanza nuestra excepción si los datos son incorrectos
public void validar() throws PedidoInvalidoException {
if (producto == null || producto.trim().isEmpty()) {
throw new PedidoInvalidoException("El nombre del producto no puede estar vacío");
}
if (cantidad <= 0) {
throw new PedidoInvalidoException("Cantidad debe ser mayor a cero");
}
if (precioUnitario <= 0) {
throw new PedidoInvalidoException("El precio unitario debe ser mayor a cero");
}
}

// Función pura: Calcula el subtotal multiplicando cantidad por precio unitario
public double subtotal() {
    return cantidad * precioUnitario;
}


}


            <!-- Code 3: ProcesadorServicio -->
            <div id="code-block-servicio" class="code-container hidden">
                <div class="text-xs text-slate-500 mb-1 font-mono">Paquete: com.odinsoft.servicio</div>
                <pre class="code-block p-4 rounded-xl text-xs overflow-x-auto"><code>package com.odinsoft.servicio;


import com.odinsoft.modelo.Pedido;
import com.odinsoft.modelo.PedidoInvalidoException;

import java.util.*;
import java.util.function.Function;
import java.util.stream.Collectors;

public class ProcesadorServicio {

// 1. FÁBRICA DE FUNCIONES: Retorna la lógica de descuento según el monto
public static Function&lt;Pedido, Double&gt; obtenerPoliticaDescuento() {
    return pedido -&gt; {
        double subtotal = pedido.subtotal();
        if (subtotal &gt; 1000.0) return 0.10; // 10% de descuento
        if (subtotal &gt; 500.0) return 0.05;  // 5% de descuento
        return 0.0;                         // Sin descuento
    };
}

// 2. FUNCIÓN DE ORDEN SUPERIOR: Recibe la función de descuento como parámetro
public static double calcularMontoConDescuento(Pedido pedido, Function&lt;Pedido, Double&gt; calculadora) {
    double subtotal = pedido.subtotal();
    double descuento = calculadora.apply(pedido);
    return subtotal * (1 - descuento);
}

// 3. FILTER: Separar pedidos válidos
public static List&lt;Pedido&gt; obtenerPedidosValidos(List&lt;Pedido&gt; pedidos) {
    return pedidos.stream()
            .filter(p -&gt; {
                try {
                    p.validar();
                    return true;
                } catch (PedidoInvalidoException e) {
                    return false;
                }
            })
            .toList(); 
}

// 4. MAP y REDUCE: Sumar todos los montos finales
public static double calcularTotalFacturado(List&lt;Pedido&gt; pedidosValidos) {
    Function&lt;Pedido, Double&gt; politica = obtenerPoliticaDescuento();
    
    return pedidosValidos.stream()
            .map(p -&gt; calcularMontoConDescuento(p, politica))
            .reduce(0.0, Double::sum); 
}

// 5. GROUPING BY: Agrupar por región
public static Map&lt;String, Double&gt; agruparPorRegion(List&lt;Pedido&gt; pedidosValidos) {
    Function&lt;Pedido, Double&gt; politica = obtenerPoliticaDescuento();

    return pedidosValidos.stream()
            .collect(Collectors.groupingBy(
                    Pedido::region,
                    Collectors.summingDouble(p -&gt; calcularMontoConDescuento(p, politica))
            ));
}


}


            <!-- Code 4: GUI FormularioApp -->
            <div id="code-block-gui" class="code-container hidden">
                <div class="text-xs text-slate-500 mb-1 font-mono">Paquete: com.odinsoft.gui</div>
                <pre class="code-block p-4 rounded-xl text-xs overflow-x-auto"><code>package com.odinsoft.gui;


import com.odinsoft.modelo.Pedido;
import com.odinsoft.servicio.ProcesadorServicio;

import javax.swing.;
import java.awt.;
import java.util.ArrayList;
import java.util.List;

public class FormularioApp extends JFrame {

private final List&lt;Pedido&gt; listaPedidos = new ArrayList&lt;&gt;();

public FormularioApp() {
    setTitle("OdinsoftNorte S.A.C. - Gestión de Pedidos Funcional");
    setSize(900, 700);
    setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    setLocationRelativeTo(null);
    // Interfaz construida con Swing...
}

public static void main(String[] args) {
    SwingUtilities.invokeLater(() -&gt; new FormularioApp().setVisible(true));
}


}


        </div>
    </section>

    <!-- SECCIÓN 4: SIMULADOR INTERACTIVO -->
    <section id="sec-simulador" class="space-y-6 hidden">
        <div class="bg-white p-6 rounded-2xl shadow-sm border border-slate-200">
            <h2 class="text-2xl font-bold text-slate-800 border-b pb-3 flex items-center gap-3">
                <span class="bg-purple-100 text-purple-700 w-10 h-10 rounded-full flex items-center justify-center text-lg"><i class="fa-solid fa-flask"></i></span>
                Simulador Interactivo de Pedidos (Prueba las Reglas)
            </h2>
            <p class="text-slate-600 mt-2">Agrega pedidos para ver cómo la lógica funcional aplica los descuentos y filtra los errores en tiempo real:</p>

            <!-- Formulario Simulador -->
            <div class="grid grid-cols-1 md:grid-cols-5 gap-3 mt-4 bg-slate-50 p-4 rounded-xl border border-slate-200">
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Cliente</label>
                    <input type="text" id="sim-cliente" value="CLI001" class="w-full text-xs p-2 border rounded border-slate-300">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Producto</label>
                    <input type="text" id="sim-producto" value="Arroz Costeño 5kg" class="w-full text-xs p-2 border rounded border-slate-300">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Cantidad</label>
                    <input type="number" id="sim-cantidad" value="30" class="w-full text-xs p-2 border rounded border-slate-300">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Precio Unitario</label>
                    <input type="number" id="sim-precio" value="50.0" class="w-full text-xs p-2 border rounded border-slate-300">
                </div>
                <div>
                    <label class="block text-xs font-bold text-slate-700 mb-1">Región</label>
                    <select id="sim-region" class="w-full text-xs p-2 border rounded border-slate-300">
                        <option value="Lima">Lima</option>
                        <option value="Provincia">Provincia</option>
                        <option value="Exportación">Exportación</option>
                    </select>
                </div>
            </div>

            <div class="flex gap-2 mt-3">
                <button onclick="agregarPedidoSimulado()" class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold text-xs py-2 px-4 rounded transition">
                    <i class="fa-solid fa-plus"></i> Agregar Pedido
                </button>
                <button onclick="cargarCasosPrueba()" class="bg-amber-500 hover:bg-amber-600 text-white font-bold text-xs py-2 px-4 rounded transition">
                    <i class="fa-solid fa-bolt"></i> Cargar Casos de Prueba
                </button>
                <button onclick="limpiarSimulador()" class="bg-slate-300 hover:bg-slate-400 text-slate-800 font-bold text-xs py-2 px-4 rounded transition ml-auto">
                    <i class="fa-solid fa-trash"></i> Limpiar Todo
                </button>
            </div>

            <!-- Tablas de Resultados Simulados -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-6">
                
                <!-- Tabla Válidos -->
                <div class="border rounded-xl p-4 bg-emerald-50/50 border-emerald-200">
                    <h3 class="font-bold text-emerald-900 text-sm mb-2 flex items-center gap-2">
                        <i class="fa-solid fa-circle-check text-emerald-600"></i> Pedidos Válidos (Procesados)
                    </h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left text-xs bg-white rounded border">
                            <thead class="bg-emerald-100 text-emerald-900 font-bold border-b">
                                <tr>
                                    <th class="p-2">Producto</th>
                                    <th class="p-2">Cant x Precio</th>
                                    <th class="p-2">Región</th>
                                    <th class="p-2">Monto Final</th>
                                </tr>
                            </thead>
                            <tbody id="tbody-validos">
                                <tr><td colspan="4" class="p-3 text-center text-slate-400">Sin datos registrados</td></tr>
                            </tbody>
                        </table>
                    </div>
                </div>

                <!-- Tabla Rechazados -->
                <div class="border rounded-xl p-4 bg-rose-50/50 border-rose-200">
                    <h3 class="font-bold text-rose-900 text-sm mb-2 flex items-center gap-2">
                        <i class="fa-solid fa-circle-xmark text-rose-600"></i> Pedidos Rechazados (Errores)
                    </h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left text-xs bg-white rounded border">
                            <thead class="bg-rose-100 text-rose-900 font-bold border-b">
                                <tr>
                                    <th class="p-2">Producto</th>
                                    <th class="p-2">Motivo de Rechazo</th>
                                </tr>
                            </thead>
                            <tbody id="tbody-rechazados">
                                <tr><td colspan="2" class="p-3 text-center text-slate-400">Sin errores registrados</td></tr>
                            </tbody>
                        </table>
                    </div>
                </div>

            </div>

            <!-- Resumen de Métricas -->
            <div class="bg-slate-800 text-slate-100 p-4 rounded-xl text-xs space-y-2 mt-4 font-mono">
                <div class="font-bold text-amber-400">RESUMEN ESTADÍSTICO (STREAMS/REDUCE):</div>
                <div>TOTAL FACTURADO: <span id="res-total" class="font-bold text-emerald-400">S/ 0.00</span></div>
                <div>POR REGIÓN: <span id="res-region" class="text-slate-300">Sin datos</span></div>
                <div>PEDIDO MAYOR MONTO: <span id="res-mayor" class="text-cyan-300">Ninguno</span></div>
            </div>

        </div>
    </section>

</main>

<footer class="text-center text-slate-500 text-xs py-6 border-t border-slate-200 mt-12">
    OdinsoftNorte S.A.C. &copy; Guía Educativa de Programación Funcional en Java
</footer>

<!-- Lógica JavaScript Interactiva -->
<script>
    function showTab(tabName) {
        document.querySelectorAll('main > section').forEach(sec => sec.classList.add('hidden'));
        document.getElementById('sec-' + tabName).classList.remove('hidden');
        
        document.querySelectorAll('.tab-btn').forEach(btn => {
            btn.classList.remove('bg-indigo-600', 'text-white');
            btn.classList.add('bg-white', 'text-slate-700');
        });

        const activeBtn = document.getElementById('btn-' + tabName);
        activeBtn.classList.remove('bg-white', 'text-slate-700');
        activeBtn.classList.add('bg-indigo-600', 'text-white');
    }

    function showCode(codeName) {
        document.querySelectorAll('.code-container').forEach(c => c.classList.add('hidden'));
        document.getElementById('code-block-' + codeName).classList.remove('hidden');

        document.querySelectorAll('.code-tab-btn').forEach(btn => {
            btn.classList.remove('bg-slate-800', 'text-white');
            btn.classList.add('bg-slate-200', 'text-slate-700');
        });

        const activeBtn = document.getElementById('code-btn-' + codeName);
        activeBtn.classList.remove('bg-slate-200', 'text-slate-700');
        activeBtn.classList.add('bg-slate-800', 'text-white');
    }

    // LÓGICA DEL SIMULADOR
    let pedidos = [];

    function agregarPedidoSimulado() {
        const cliente = document.getElementById('sim-cliente').value;
        const producto = document.getElementById('sim-producto').value;
        const cantidad = parseInt(document.getElementById('sim-cantidad').value) || 0;
        const precio = parseFloat(document.getElementById('sim-precio').value) || 0;
        const region = document.getElementById('sim-region').value;

        pedidos.push({ cliente, producto, cantidad, precio, region });
        procesarSimulador();
    }

    function cargarCasosPrueba() {
        pedidos = [
            { cliente: 'CLI01', producto: 'Azúcar 10kg', cantidad: 10, precio: 50.0, region: 'Lima' },
            { cliente: 'CLI02', producto: 'Aceite Primor 1L', cantidad: 30, precio: 50.0, region: 'Lima' }, // 10% desc -> 1350
            { cliente: 'CLI03', producto: 'Fideos Don Vittorio', cantidad: -5, precio: 20.0, region: 'Provincia' }, // Error
            { cliente: 'CLI04', producto: '', cantidad: 10, precio: 15.0, region: 'Exportación' } // Error
        ];
        procesarSimulador();
    }

    function limpiarSimulador() {
        pedidos = [];
        procesarSimulador();
    }

    function procesarSimulador() {
        const tbodyValidos = document.getElementById('tbody-validos');
        const tbodyRechazados = document.getElementById('tbody-rechazados');
        
        tbodyValidos.innerHTML = '';
        tbodyRechazados.innerHTML = '';

        let validos = [];
        let rechazados = [];

        // Validación funcional simulada
        pedidos.forEach(p => {
            if (!p.producto || p.producto.trim() === '') {
                rechazados.push({ p, motivo: 'El nombre del producto no puede estar vacío' });
            } else if (p.cantidad <= 0) {
                rechazados.push({ p, motivo: 'Cantidad debe ser mayor a cero' });
            } else if (p.precio <= 0) {
                rechazados.push({ p, motivo: 'Precio debe ser mayor a cero' });
            } else {
                // Cálculo descuento
                const subtotal = p.cantidad * p.precio;
                let desc = 0;
                if (subtotal > 1000) desc = 0.10;
                else if (subtotal > 500) desc = 0.05;
                const montoFinal = subtotal * (1 - desc);

                validos.push({ ...p, subtotal, desc, montoFinal });
            }
        });

        // Render Válidos
        if (validos.length === 0) {
            tbodyValidos.innerHTML = '<tr><td colspan="4" class="p-3 text-center text-slate-400">Sin datos válidos</td></tr>';
        } else {
            validos.forEach(v => {
                tbodyValidos.innerHTML += `
                    <tr class="border-b text-slate-700">
                        <td class="p-2 font-semibold">${v.producto}</td>
                        <td class="p-2">${v.cantidad} x S/ ${v.precio.toFixed(2)}</td>
                        <td class="p-2">${v.region}</td>
                        <td class="p-2 font-bold text-emerald-700">S/ ${v.montoFinal.toFixed(2)} (${v.desc*100}% desc)</td>
                    </tr>
                `;
            });
        }

        // Render Rechazados
        if (rechazados.length === 0) {
            tbodyRechazados.innerHTML = '<tr><td colspan="2" class="p-3 text-center text-slate-400">Sin errores</td></tr>';
        } else {
            rechazados.forEach(r => {
                tbodyRechazados.innerHTML += `
                    <tr class="border-b text-slate-700">
                        <td class="p-2 font-semibold">${r.p.producto || '(Vacío)'}</td>
                        <td class="p-2 text-rose-600 font-bold">${r.motivo}</td>
                    </tr>
                `;
            });
        }

        // Métricas (Reduce & GroupingBy)
        const totalFacturado = validos.reduce((acc, curr) => acc + curr.montoFinal, 0);
        document.getElementById('res-total').innerText = `S/ ${totalFacturado.toFixed(2)}`;

        // Grouping by region
        const regiones = {};
        validos.forEach(v => {
            regiones[v.region] = (regiones[v.region] || 0) + v.montoFinal;
        });

        let regText = Object.keys(regiones).map(r => `${r}: S/ ${regiones[r].toFixed(2)}`).join(' | ') || 'Sin datos';
        document.getElementById('res-region').innerText = regText;

        // Mayor
        if (validos.length > 0) {
            const mayor = validos.reduce((prev, current) => (prev.montoFinal > current.montoFinal) ? prev : current);
            document.getElementById('res-mayor').innerText = `${mayor.producto} (S/ ${mayor.montoFinal.toFixed(2)})`;
        } else {
            document.getElementById('res-mayor').innerText = 'Ninguno';
        }
    }
</script>
