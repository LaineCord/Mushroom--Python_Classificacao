# Em construção 

# Mushroom

# 1. Sobre o Dataset

Este conjunto de dados inclui descrições de amostras hipotéticas correspondentes a 23 espécies de cogumelos com guelras na Família Agaricus e Lepiota (pp. 500-525). Cada espécie é identificada como definitivamente comestível, definitivamente venenosa ou de comestibilidade desconhecida e não recomendada. Esta última classe foi combinada com a venenosa. O Guia afirma claramente que não há uma regra simples para determinar a comestibilidade de um cogumelo; nenhuma regra como ``folhetos três, deixe estar'' para Carvalho Venenoso e Hera.

## 1. 2 Sobre a espécie Agaricus

Nome científico: Agaricus sp.
Família: Agaricaceae
Distribuição geográfica: Cosmopolita
Características morfológicas: Apresenta basidioma macio de tamanho médio a grande; o chapéu é hemisférico inicialmente, depois convexo e finalmente mais ou menos aplanado ou ligeiramente deprimido, de cor esbranquiçada ou parda. O pé (estipe) é cilíndrico, tanto regular como engrossado ou atenuado para a base; sempre porta um anel, mais ou menos desenvolvido, que pode ser persistente ou caduco e se separa com facilidade da carne do chapéu.
Características interessantes: O gênero Agaricus é um importante gênero de cogumelos, contendo tanto espécies comestíveis como venenosas. Uma de suas espécies é o cogumelo comum (champignon de Paris, Agaricus bisporus). Algumas espécies, como Agaricus blazei, têm sido estudadas porque contém complexos de polissacarídeo-proteína que podem apresentar atividade no sistema imunológico humano entre outras utilidades medicinais.

Fonte: https://museunacional.ufrj.br/hortobotanico/Fungos/Agaricus.html
## 1.3. Sobre a espécie Lepiota

Nome cientigico: Lepiota sp.
Família: Agaricaceae
Características morfológicas: Tipicamente têm aneis nos estipes, os quais, nas espécies maiores, são soltos podendo deslizar para cima e para baixo ao longo do pé. O píleo normalmente tem escamas: as cores do píleo, lamelas e escamas são importantes na determinação exacta da espécies, bem como por vezes o odor.

Fonte: https://www.inaturalist.org/taxa/58695-Lepiota

# 2. Objetivo do Estudo: Classificar Cogumelos tóxicos de comestíveis
# 3. Variáveis encontradas no Dataset¶
![image](https://github.com/user-attachments/assets/255257d1-a7e3-4937-902e-3229e2611045)

1. cap-shape (Formato do chapéu):         bell=b,conical=c,convex=x,flat=f, knobbed=k,sunken=s

2. cap-surface (Superfície do chapéu):    fibrous=f,grooves=g,scaly=y,smooth=s

3. cap-color (Cor do chapéu):             brown=n,buff=b,cinnamon=c,gray=g,green=r, pink=p,purple=u,red=e,white=w,yellow=y

4. bruises? (Machucados):                 bruises=t,no=f

5. odor (Odor):                           almond=a,anise=l,creosote=c,fishy=y,foul=f, musty=m,none=n,pungent=p,spicy=s

6. gill-attachment (Fixação de Gueiras):  attached=a,descending=d,free=f,notched=n

7. gill-spacing (Espaçamento de gueiras): close=c,crowded=w,distant=d

8. gill-size (Tamanho de Gueiras):        broad=b,narrow=n

9. gill-color (Cor de Gueiras):           black=k,brown=n,buff=b,chocolate=h,gray=g,green=r,orange=o,pink=p,purple=u,red=e, white=w,yellow=y

10. stalk-shape (Formato de talo):        enlarging=e,tapering=t

11. stalk-root (Raiz de talo):            bulbous=b,club=c,cup=u,equal=e, rhizomorphs=z,rooted=r,missing=?

12. stalk-surface-above-ring (Suerfície de talo acima do anel): fibrous=f,scaly=y,silky=k,smooth=s

13. stalk-surface-below-ring (Superfície de talo abaixo do anel): fibrous=f,scaly=y,silky=k,smooth=s

14. stalk-color-above-ring (Cor de talo acima do anel):   brown=n,buff=b,cinnamon=c,gray=g,orange=o, pink=p,red=e,white=w,yellow=y

15. stalk-color-below-ring (Cor-de-talo-abaixo-do-anel):   brown=n,buff=b,cinnamon=c,gray=g,orange=o, pink=p,red=e,white=w,yellow=y

16. veil-type (Tipo de véu):               partial=p,universal=u

17. veil-color (Cor de véu):               brown=n,orange=o,white=w,yellow=y

18. ring-number (Número de anel):          none=n,one=o,two=t

19. ring-type (Tipo de anel):              cobwebby=c,evanescent=e,flaring=f,large=l, none=n,pendant=p,sheathing=s,zone=z

20. spore-print-color (cor de impressao de esporos):        black=k,brown=n,buff=b,chocolate=h,green=r, orange=o,purple=u,white=w,yell

21. population (População):               abundant=a,clustered=c,numerous=n, scattered=s,several=v,solitary=y

22. habitat (Habitat):                    grasses=g,leaves=l,meadows=m,paths=p, urban=u,waste=w,woods=d


__Variaveis Target__

edible=e poisonous=p


# 4. Avaliando o Modelo de Classificação
## 4.1 Matriz Confusão
![Sem título](https://github.com/user-attachments/assets/071e50a5-5d62-4dcc-a864-77646d0fe7eb)

O modelo está predominantemente com altos Verdadeiros Positivos (TP) e Verdadeiros Negativos (TN) o que indica que está classificando corretamente a maioria dos casos.

## 4.2 Métricas de desempenho
![image](https://github.com/user-attachments/assets/322cdb4a-42f2-4167-81dc-515ab99360bb)

- A Acuracia(Accuracy: mede a proporção total de previsões corretas. No caso do modelo em questão, a acuracia esta em 97%, o que demonstra uma boa previsibilidade. Apesar da acuracia já indicar uma boa previsibilidade é importante análisar outras métricas para entender se, de fato, o modelo esta se comportando bem.
- A precisão(Precision): mede a proporção de verdadeiros positivos entre todos os previstos pelo modelo, ou seja, o quão provavel é em classificar corretamente as previsões. Neste caso, o modelo demonstra uma grande capacidade, visto que esta entre 97 - 98 %.
- A Revocação(Recall): mede a força do modelo em prever um resultado positivo. No modelo em questão, a previsão esta entre 97 - 98%, o que indica uma ótima previsibilidade.
- F1-Score: mede o quanto a precisão e a revocação estão sendo eficientes. No caso em questão vemos uma boa eficiência entre os dois casos.

## 4.3 Distribuição das Classes
![image](https://github.com/user-attachments/assets/5cac7bd7-5ad4-498e-8ff3-7d68e038e7d8)

A distribuição de classes tem uma diferença de 3%, o que esta dentro do aceitável para o desenvolvimento de um modelo de classificação.

## 4.4  Validação Cruzada
![image](https://github.com/user-attachments/assets/364f0963-b039-464b-87a4-9a5bbe058985)

## 4.5 AUC
![image](https://github.com/user-attachments/assets/7e555bb9-0889-495a-b184-df372b566964)

O modelo possui uma métrica de área sob a curva (AUC) de 0.9738, correspondendo a um classificador relativamente bom, logo que quanto mais próximo de 1, melhor ele é.

## 5. Fonte do DataSet
https://archive.ics.uci.edu/dataset/73/mushroom