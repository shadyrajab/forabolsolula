# **Contribuindo para o repositório**
O objetivo desse documento é ser um guia para pessoas querendo contribuir com o site. Há várias maneiras de contribuir, alguns exemplo são:
*   Adicionar funcionalidades ao site;
*   Encontrar erros de digitação e os corrigir;
*   Adicionar uma traição do Bolsonaro ou crime do Lula que pode estar faltando;
*   etc...


## **Como contribuir**

### **Evite commits na branch master.**

### **Para adicionar funcionalidades:**
*   Faça um fork do repositório e crie uma branch onde seram feitas as modificações. Tente dar um nome curto e descritivo a branch, se possível;

*   Depois de implementada(s) a(s) funcionalidade(s), volte para branch principal e atualize-a com `git fetch upstream && git merge upstream/master`;

*   Faça o *merge* com `git merge <nome_da_branch>`, substituindo <nome_da_branch> pelo nome da branch com as novas funcionalidades;

*   Resolva os possíveis conflitos que podem surgir, e atualize sua fork com `git push origin master`;

*   Em seu fork no github, crie um pull request descritivo e em breve suas alterações estaram no site :)


### **Caso não saiba programação, mas queira ajudar de alguma maneira:**

*   Vá para a aba [Issues](https://github.com/shadyrajab/forabolsolula/issues) e procure para ver se há uma issue parecida; 

*   Se não houver, crie uma issue com um título curto e descritivo. Se julgar necessário, descreva mais profundamente sua sugestão com comentários;

*   Os desenvolvedores julgaram se a issue é pertinente ou não. Caso seja, trabalharão nela e assim que terminarem a marcarão como fechada.