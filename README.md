# 🗳️ Simulador de Eleição por Preferência (Segundo Turno)  

Este programa em C implementa um **sistema de votação por preferência** (Ranked Choice Voting), onde os eleitores classificam os candidatos em ordem de preferência. Se nenhum candidato obtiver a maioria absoluta no primeiro turno, o candidato com menos votos é eliminado e os votos são redistribuídos até que haja um vencedor.  

## 📌 Funcionalidades  
- ✅ Os eleitores podem classificar os candidatos em ordem de preferência.  
- ✅ O sistema elimina o candidato com menos votos em cada rodada e redistribui os votos.  
- ✅ O processo continua até que um candidato obtenha mais da metade dos votos válidos.  
- ✅ Se houver empate entre os candidatos restantes, todos os empatados são declarados vencedores.  

## 📥 Como Compilar e Executar  

1. **Compile o código** usando o `clang` ou `gcc`:  
   ```sh
   clang -o eleicao_preferencial eleicao_preferencial.c -lcs50
   ```  
   ou  
   ```sh
   gcc -o eleicao_preferencial eleicao_preferencial.c -lcs50
   ```  
   
2. **Execute o programa** especificando os candidatos na linha de comando:  
   ```sh
   ./eleicao_preferencial Alice Bob Charlie  
   ```  
   
3. **Informe o número de eleitores** e classifique os candidatos em ordem de preferência.  

4. O sistema processará os votos e exibirá o vencedor! 🎉  

## 📖 Exemplo de Uso  
```sh
$ ./eleicao_preferencial Alice Bob Charlie  
NUMERO DE ELEITORES: 5  
CLASSIFICAÇÃO 1: Alice  
CLASSIFICAÇÃO 2: Charlie  
CLASSIFICAÇÃO 3: Bob  

CLASSIFICAÇÃO 1: Bob  
CLASSIFICAÇÃO 2: Alice  
CLASSIFICAÇÃO 3: Charlie  

... (demais votos)  

RESULTADO Alice 🎉  
```  

## ⚠️ Regras e Limitações  
- Deve haver pelo menos **dois candidatos**.  
- O número máximo de candidatos permitidos é **9**.  
- O número máximo de eleitores suportados é **100**.  
- Se um candidato receber mais da metade dos votos no primeiro turno, ele vence imediatamente.  
- Se todos os candidatos restantes tiverem a mesma quantidade de votos, há um **empate**.  

## 🛠️ Estrutura do Código  
O código contém as seguintes funções principais:  

- `vote()`: Registra a ordem de preferência dos eleitores.  
- `tabulate()`: Conta os votos para os candidatos ainda não eliminados.  
- `print_winner()`: Verifica se algum candidato tem mais da metade dos votos.  
- `find_min()`: Encontra o menor número de votos entre os candidatos restantes.  
- `is_tie()`: Verifica se há empate entre todos os candidatos restantes.  
- `eliminate()`: Elimina o(s) candidato(s) com menos votos.  

## 📜 Licença  
Este projeto é de código aberto e pode ser modificado e distribuído livremente.  

---
## REDME creado por IA 
