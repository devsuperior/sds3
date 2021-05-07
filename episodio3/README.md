# ![DevSuperior logo](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/devsuperior-logo-small.png) Semana Spring React - Episódio 3
> Evento gratuito - 3 a 9 de maio/2021
> 
>  *Crie um app inédito para seu portfólio com as tecnologias mais demandadas do mercado*

## Realização
[DevSuperior - Escola de programação](https://devsuperior.com.br)

[![DevSuperior no Instagram](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/ig-icon.png)](https://instagram.com/devsuperior.ig)
[![DevSuperior no Youtube](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/yt-icon.png)](https://youtube.com/devsuperior)

## Objetivos do projeto para esta aula
- Integrar back end e front end
- Três pilares do React
  - Componentes
  - Props
  - Estado
- React Hooks
  - useState
  - useEffect
- Libs
  - React Router DOM
  - Axios

## Checklist

- **AVISO: as aulas ficarão disponíveis somente até dia 9 às 23h59**
- **AVISO: como obter o certificado?**
  - https://github.com/devsuperior/sds3/tree/main/_certificado

- **AVISO: entrar no Discord do evento**
  - https://discord.gg/Y8UZCX8Zmh
  - Apresente-se em `#papo-e-networking`
  - Fique de olho em `#duvidas-frequentes`

### Passo 1: Rotas

- Instalar React Router DOM
```bash
yarn add react-router-dom

yarn add @types/react-router-dom -D
```
- Criar páginas Home e Dashboard
- Criar arquivo de rotas `Routes.tsx`
- **COMMIT: Routes**

### Passo 2: Página Home e navegações

```html
<div className="container">
    <div className="jumbotron">
        <h1 className="display-4">DSVendas</h1>
        <p className="lead">Analise o desempenho das suas vendas por diferentes perspectivas</p>
        <hr/>
        <p>Esta aplicação consiste em exibir um dashboard a partir de dados fornecidos por um back end construído com Spring Boot.</p>
    </div>
</div>
```
- Fazer um link na Home para Dashboard
- Fazer um link na NavBar para Home

- **COMMIT: Home, navigation**

### Passo 3: First request

- Instalar Axios
```bash
yarn add axios
```
- Definir BASE_URL
- Definir tipo SaleSum
- Definir tipo local ChartData em DonutChart
- Fazer a requisição e tratar os dados

- **COMMIT: First request**

### Passo 4: DonutChart integration

```
Hook: useState
Manter estado no componente
```
```
Hook: useEffect
Executar algo na instanciação ou destruição do componente, observar estado
```

- **COMMIT: DonutChart integration**

### Passo 5: BarChart integration

- Definir função auxiliar round:
```javascript
export const round = (value: number, precision: number) => {
    var multiplier = Math.pow(10, precision || 0);
    return Math.round(value * multiplier) / multiplier;
}
```

- Definir tipo SaleSuccess
- Definir tipo local ChartData em DonutChart

- **COMMIT: BarChart integration**

### Passo 6: DataTable integration

- Instalar date-fns ao projeto
```bash
yarn add date-fns
```
- Criar tipos Seller, Sale, SalePage
- Criar função auxiliar formatLocalDate
```javascript
export const formatLocalDate = (date: string, pattern: string) => {
    const dt = new Date(date);
    const dtDateOnly = new Date(dt.valueOf() + dt.getTimezoneOffset() * 60 * 1000);
    return format(dtDateOnly, pattern);
}
```

- **COMMIT: DataTable integration**

### Passo 7: Pagination

```
Props
Argumentos que um componente React pode receber
```

- Criar componente Pagination
```html
<div className="row d-flex justify-content-center">
    <nav>
        <ul className="pagination">
            <li className="page-item">
                <button className="page-link">Anterior</button>
            </li>
            <li className="page-item disabled">
                <span className="page-link">1</span>
            </li>
            <li className="page-item disabled">
                <button className="page-link">Próxima</button>
            </li>
        </ul>
    </nav>
</div>
```

- **COMMIT: Pagination**

## **PARABÉNS!**

![Parabéns!](https://raw.githubusercontent.com/devsuperior/bds-assets/main/img/trophy.png)

- Quero muito saber seu feedback
  - O que você está achando da nossa abordagem?
  - Você está conseguindo acompanhar?
  - O que você está achando do evento?
- Participe
  - Comente na página da Semana Spring React
  - Divulgue seu projeto no Linkedin e marque a DevSuperior

