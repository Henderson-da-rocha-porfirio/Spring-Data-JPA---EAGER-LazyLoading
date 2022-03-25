#Lazy Load

### Lazy Loading acontece onde o dado na associação está sendo buscado sob-demanda e quando ele foi usado primeiro. E quando o objeto Pai é lido, não será lido corretamente.
### Então, habilitar lazy loading na aplicação nas anotações que nós usamos como se fosse OneToMany:
### Pai: @OneToMany(fetch=FetchType.EAGER) => fetch é um atributo que pega dois valores FetchType ( é uma enumeração ) que tem dois valores: EAGER que buscará o dado corretamente assim que o Pai for lido.
### Filho: @ManyToMany(fetch=FetchType.LAZY) => O filho também será lido e o dado será buscado lentamente ( lazy ).
## Ex: Pessoa						
### List < NumeroTelefone > numerosTelefone;
### Lazy Loading 			getNumerosTelefone
