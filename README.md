# php-composer-buscador-cursos

- Usando o [composer](https://getcomposer.org/);
- Para buscar pacotes ver [packagist](https://packagist.org/);
- Para esse exemplo foram utilizadas duas bibliotecas externas:
  * Para o client http [guzzlehttp/guzzle](https://packagist.org/packages/guzzlehttp/guzzle);
  * Para trabalhar com o DOM [symfony/dom-crawler](https://packagist.org/packages/symfony/dom-crawler);
- Comandos do composer:
  * Executar a partir da pasta raiz do projeto;
  * Para instalar um novo pacote:
    ```
    composer require guzzlehttp/guzzle
    ```
  * Para instalar pacotes incluidos manualmente no 'composer.json' ou para restaurar pacotes em um projeto recém baixado:
    ```
    composer install
    ou
    composer update
    ```
  * Para atualizar o 'vendor/autoload.php' para registrar a mudança do 'composer.json' (devido a inclusão de uma 'psr-4' por exemplo) sem o uso do 'install' ou do 'update':
    ```
    composer dumpautoload
    ```
  * Para instalar no projeto ferramentas para auxiliar no desenvolvimento, ou seja, algo que não será disponibilizado ao cliente como uma ferramenta de testes por exemplo:
    ```
    composer require --dev phpunit/phpunit ^9.3
    ```
  * Para usar ferramentas que auxiliam no desenvolvimento:
    + Execução de testes (considerando um script chamado "test"):
      ```
      composer run test
      ```
    + Verificar se o código esta no padrão:
      ```
      vendor\bin\phpcs --standard=PSR12 src\
      ```
    + Verificar erros no código
      ```
      vendor\bin\phan --allow-polyfill-parser
      ```
