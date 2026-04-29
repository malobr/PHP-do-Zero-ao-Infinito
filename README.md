# PHP do Zero ao Infinito: O Despertar da Engenharia

Este repositório registra minha jornada de reconstrução técnica. Após perceber a dependência excessiva de ferramentas de geração de código, decidi resetar meu conhecimento e aprender **PHP Real**, do zero, utilizando apenas as fontes que formaram os maiores programadores da última década.

##  O Manifesto: Por que este método?

1.  **Sem IA (Anti-Gravity/ChatGPT/Copilot):** A IA entrega a resposta, mas rouba o aprendizado. Ao ler a documentação, eu entendo o *porquê*, não apenas o *como*.
2.  **Documentação Oficial como Bíblia:** Onde a verdade reside. Se não está no PHP.net, não existe.
3.  **Stack Overflow para Depuração:** Aprender a ler o erro de outros desenvolvedores e filtrar soluções é uma habilidade vital.
4.  **Docker Only:** Sem facilitadores (XAMPP/WAMP). O ambiente deve replicar um servidor de produção real no Linux.

## Fontes de Consulta Permitidas
* [Documentação Oficial do PHP (Manual)](https://www.php.net/manual/pt_BR/)
* [Stack Overflow (Global)](https://stackoverflow.com/questions/tagged/php)

---

##  O Ambiente de Desenvolvimento
O projeto roda inteiramente em **Docker**.
* **PHP 8.3-FPM** (Base Alpine)
* **Nginx**
* **MySQL 8.0** (Persistência de dados)
* **Redis** (Cache e Filas)

---

## 🚀 O Caminho das 50 Provações (Checklist de Desafios)

### **Nível 1: Fundamentos e Sintaxe**
- [ ] 01. **Hello World & `phpinfo()`**: Configurar o Docker e garantir que o Nginx serve PHP.
- [ ] 02. **Manipulação de Tipos**: Criar um script que recebe dados via URL (`$_GET`) e faz casting explícito.
- [ ] 03. **Calculadora de Precisão**: Usar `bcmath` para cálculos financeiros sem erros de float.
- [ ] 04. **Gerador de Tabela HTML**: Um loop que gera uma tabela dinâmica baseada em um Array multidimensional.
- [ ] 05. **Validador de CPF/CNPJ**: Lógica pura de cálculos de dígitos verificadores.
- [ ] 06. **Manipulador de Strings**: Criar um "Slugificador" de URLs manualmente (sem Regex primeiro, depois com Regex).
- [ ] 07. **Sistema de Login via Array**: Hardcoded, apenas para entender `$_SESSION` e `setcookie()`.
- [ ] 08. **Fibonacci Recursivo**: Entender o custo de memória de funções recursivas.
- [ ] 09. **Explode/Implode Manual**: Criar funções que imitam as nativas para entender ponteiros de string.
- [ ] 10. **Tratamento de Erros**: Criar um `set_error_handler` personalizado que salva logs em arquivo `.log`.

### **Nível 2: POO e Estruturas**
- [ ] 11. **Classe Pessoa & Herança**: Criar `Pessoa`, `Fisica` e `Juridica`.
- [ ] 12. **Interfaces de Pagamento**: Criar uma interface e implementá-la em classes `Pix` e `Boleto`.
- [ ] 13. **Dependency Injection Manual**: Injetar uma classe de Log dentro de uma classe de Usuario.
- [ ] 14. **Trait de Auditoria**: Uma Trait que registra quem criou/editou um objeto.
- [ ] 15. **Namespaces & Autoload**: Configurar o `composer.json` para carregar suas classes via PSR-4.
- [ ] 16. **Exceptions Customizadas**: Criar uma hierarquia de exceções para uma conta bancária.
- [ ] 17. **DTO (Data Transfer Objects)**: Criar objetos para transportar dados de um formulário.
- [ ] 18. **Enums no PHP 8**: Usar Enums para status de pedidos (Pendente, Pago, Cancelado).
- [ ] 19. **Abstract Factory**: Criar uma fábrica de componentes de interface (Botão, Input).
- [ ] 20. **Singleton de Configuração**: Uma classe que carrega o `.env` e garante uma única instância.

### **Nível 3: Persistência com MySQL e Web**
- [ ] 21. **Conexão PDO**: Singleton para gerenciar a conexão segura com MySQL.
- [ ] 22. **CRUD de Produtos**: Sem frameworks. SQL Puro (Insert, Select, Update, Delete).
- [ ] 23. **Query Builder Simples**: Criar uma classe que monta a string `SELECT * FROM table WHERE...`.
- [ ] 24. **Upload de Arquivos**: Sistema com validação de MIME-type e redimensionamento de imagem (GD Library).
- [ ] 25. **Middleware de Autenticação**: Um script que intercepta todas as requisições e verifica o cookie.
- [ ] 26. **Paginação de Resultados**: Lógica de `OFFSET` e `LIMIT` no SQL para grandes listas.
- [ ] 27. **Filtros Dinâmicos**: Criar uma busca que aceita múltiplos parâmetros opcionais no MySQL.
- [ ] 28. **Transações Bancárias**: Uso de `beginTransaction`, `commit` e `rollBack` no PDO.
- [ ] 29. **Sistema de Tags (Many-to-Many)**: Lógica de tabelas pivot para relacionar posts e tags.
- [ ] 30. **Relatório em CSV**: Exportar dados do MySQL diretamente para um arquivo baixável.

### **Nível 4: Arquitetura e Performance**
- [ ] 31. **Hydrator Manual**: Converter arrays de banco de dados em objetos de classe automaticamente.
- [ ] 32. **Cache com Redis**: Salvar o resultado de uma query pesada no Redis por 60 segundos.
- [ ] 33. **Event Dispatcher**: Sistema que dispara um evento "UserRegistered" e envia e-mail/log.
- [ ] 34. **Service Container (DIC)**: Criar um container que resolve dependências via Reflection API.
- [ ] 35. **CLI Tool**: Criar um script que roda via terminal (`bin/console`) para limpar cache.
- [ ] 36. **Fila de E-mails**: Jogar tarefas no Redis e criar um "Worker" (loop infinito) para processar.
- [ ] 37. **JWT Handshake**: Gerar e validar um token JWT manualmente sem bibliotecas.
- [ ] 38. **API Restful**: Criar endpoints que respondem JSON e tratam verbos (GET, POST, PUT, DELETE).
- [ ] 39. **Rate Limiter**: Impedir que um IP faça mais de X requisições por minuto usando Redis.
- [ ] 40. **Template Engine**: Criar um sistema simples que substitui `{{ variavel }}` por PHP real.

### **Nível 5: O Ápice (O Arquiteto)**
- [ ] 41. **ORM Simplificado**: Implementar o padrão Active Record ou Data Mapper do zero.
- [ ] 42. **Injeção de Dependência por Atributos**: Usar Attributes do PHP 8 para configurar serviços.
- [ ] 43. **Integração com Gateway de Pagamento**: Simular um checkout transparente com Webhooks.
- [ ] 44. **Websockets com Ratchet**: Criar um chat em tempo real rodando em um container separado.
- [ ] 45. **Otimização de Opcache**: Configurar o ambiente para máxima performance e medir com `microtime()`.
- [ ] 46. **Static Analysis**: Configurar o PHPStan no nível máximo e corrigir todos os erros.
- [ ] 47. **Unit Testing (PHPUnit)**: Escrever testes para toda a lógica de negócio do nível 4.
- [ ] 48. **Análise de Logs com ELK**: Enviar logs do PHP para o Elasticsearch (via Docker).
- [ ] 49. **Microserviço de Autenticação**: Separar o login em um container e comunicar via cURL/gRPC.
- [ ] 50. **O Framework**: Unir os desafios anteriores e criar seu próprio mini-framework MVC funcional.

---
*"O código que você escreve sem ajuda é o único que realmente te pertence."*
