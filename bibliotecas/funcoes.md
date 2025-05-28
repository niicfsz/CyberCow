```C
#ifndef FUNCOESAP2_H_INCLUDED
#define FUNCOESAP2_H_INCLUDED
double mediaGanho(float ganhoTotal, int numeroDeVendas) {
    return ganhoTotal / numeroDeVendas;
}

double mediaGastoAlimentacao(int numeroAnimais, float precoRacao, int numeroComprasRacao) {

    return precoRacao * numeroComprasRacao / numeroAnimais;
}

double mediaLucro(float ganhoTotal, float gastoTotal) {
    return ganhoTotal - gastoTotal;
}

double ICA(float consumoDeRacao, float ganhoPeso) {
    return consumoDeRacao / ganhoPeso;
}

int testePesoIdeal(float peso, float gastoPorKgBoi, float precoVendaKgBoi) {
    if (peso * precoVendaKgBoi >= 1.3 * gastoPorKgBoi*peso) {
        return 0; 
    } else {
        return 1; 
    }
}

#endif // FUNCOESAP2_H_INCLUDED
```
