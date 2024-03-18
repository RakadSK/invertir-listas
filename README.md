    void invertirLista(){
        elemento * iterador = this->cabeza, * anterior = nullptr, * sActual = nullptr;
        this->cola = cabeza;
        while(iterador != nullptr){
            sActual = iterador->sig;
            iterador->sig = anterior;
            anterior = iterador;
            iterador =sActual;
        };
        this->cabeza = anterior;

    }
        void appendLista(elemento * componente){
        if(this->cabeza == nullptr && this->cola == nullptr){
            this->cabeza = componente;
            this->cola = componente;
        }else{cola->sig = componente;
        cola = componente;}
    }

    
struct elemento {
    // atributos del tipo abstracto de dato
    int info;
    elemento *sig;
    int enumerar;
    // Metodos
    elemento(int i){
        this->info = i;
        this->sig = nullptr;
    }
    void mostrarElemento(int numero){
        if(numero == 0){
            cout << "(" << this->info << "," << this->sig << ")";
        }if(numero == 1){
            cout << "(" << this->info << "," << this->sig << ")" << endl;
        }
        // }if(numero == 2){
        //     cout << "(" << this->info << "," << *this->sig << ")" << endl;
        // }
    }
};
