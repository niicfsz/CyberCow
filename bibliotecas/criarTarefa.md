```C
#ifndef CRIARTAREFAS_H_INCLUDED
#define CRIARTAREFAS_H_INCLUDED
#define MAX_TAREFA 256

void criarTarefa() {
    FILE *arquivo = fopen("tarefas.txt", "a");
    if (arquivo == NULL) {
        printf("Erro ao abrir o arquivo!\n");
        return 0;
    }

    char tarefa[MAX_TAREFA];
    printf("Digite a descrição da tarefa (max %d caracteres): ", MAX_TAREFA );
    fgets(tarefa, MAX_TAREFA, stdin);
    tarefa[strcspn(tarefa, "\n")] = '\0'; // Remover o '\n' do final

    fprintf(arquivo, "%s\n", tarefa);
    fclose(arquivo);
    printf("Tarefa salva com sucesso!\n");
}

#endif // CRIARTAREFAS_H_INCLUDED
```
