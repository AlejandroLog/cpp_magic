# 🔥 ¿Por qué usar bits/stdc++.h?
Esta biblioteca permite incluir múltiples cabeceras de C++ con una sola línea, facilitando la escritura de código rápido y conciso. Aunque no es recomendable para proyectos grandes debido a la inclusión innecesaria de muchas librerías, es un recurso poderoso para resolver problemas de manera ágil.

## 🚀 ¿Qué encontrarás aquí?
✔️ Ejemplos optimizados con estructuras como `map`, `set`, `vector`, `priority_queue`, `bitset`, etc.  
✔️ Algoritmos esenciales con `sort()`, `lower_bound()`, `next_permutation()` y más.  
✔️ Trucos y optimizaciones para hacer el código más eficiente.  
✔️ Comparaciones entre el uso de `bits/stdc++.h` y las cabeceras estándar.  

---

## 📝 Ejemplos de código  

### 🔹 Uso de `set` para eliminar duplicados y ordenar caracteres  
El `set` almacena valores únicos automáticamente, eliminando duplicados y permitiendo ordenar los caracteres fácilmente.  

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    string a;
    cin >> a;

    set<char> unicos(a.begin(), a.end());
    string resultado(unicos.begin(), unicos.end());
    sort(resultado.begin(), resultado.end());

    cout << resultado;
    return 0;
}
```

### 🔹 Uso de priority_queue para obtener los valores máximos rápidamente  
Usa priority_queue para obtener el elemento más grande.

```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    priority_queue<int> pq;
    pq.push(10);
    pq.push(5);
    pq.push(20);

    cout << "El máximo es: " << pq.top() << endl;
    pq.pop();
    cout << "El siguiente máximo es: " << pq.top() << endl;

    return 0;
}

```
### 🔹 Uso de vector con sort() y reverse()
Muestra cómo ordenar y luego invertir un vector con sort() y reverse().
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    vector<int> v = {4, 1, 8, 3, 6};
    sort(v.begin(), v.end());
    reverse(v.begin(), v.end());

    for (int num : v) {
        cout << num << " ";
    }

    return 0;
}
```
### 🔹 Ordenamiento con greater<int> en sort()
Ordena el vector de mayor a menor utilizando greater<int>.
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    vector<int> v = {4, 1, 8, 3, 6};
    sort(v.begin(), v.end(), greater<int>());

    for (int num : v) {
        cout << num << " ";
    }

    return 0;
}
```
### 🔹 Búsqueda Binaria (binary_search)
La búsqueda binaria permite encontrar un elemento en un vector ordenado en tiempo logarítmico O(log n)
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    vector<int> v = {1, 3, 5, 7, 9, 11};
    int x;
    cin >> x;

    if (binary_search(v.begin(), v.end(), x)) {
        cout << "El elemento " << x << " está en el vector.\n";
    } else {
        cout << "El elemento " << x << " no está en el vector.\n";
    }

    return 0;
}
```
### 🔹 Encuentra el mínimo y máximo en un rango (min_element, max_element)
Busca el mínimo y máximo en un rango de manera eficiente.
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    vector<int> v = {4, 1, 8, 3, 6};

    auto min_it = min_element(v.begin(), v.end());
    auto max_it = max_element(v.begin(), v.end());

    cout << "Mínimo: " << *min_it << "\n";
    cout << "Máximo: " << *max_it << "\n";

    return 0;
}
```
### 🔹 Uso de pair para almacenar valores juntos
pair almacena dos valores juntos, útil en estructuras como map
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    pair<string, int> persona = {"nose", 24};
    
    cout << "Nombre: " << persona.first << ", Edad: " << persona.second << endl;
    
    return 0;
}

```
### 🔹 Uso de reverse() para invertir un vector
Invierte los elementos de un vector en tiempo O(n).
```cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    vector<int> v = {1, 2, 3, 4, 5};
    reverse(v.begin(), v.end());

    for (int num : v) {
        cout << num << " ";
    }

    return 0;
}


