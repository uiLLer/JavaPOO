Para criar um [[Método]] usamos a seguinte expressão dentro da nossa Classe:

(retorno) +  <nome_do_metodo> (<tipo_primitivo>  argumento){
	ação usando o argumento
}

um exemplo de aplicação que não retorna nada:

`void avalia(double nota){`
        `somaAvaliacao += nota;`
        `totalAvaliacao++;`
    `}`
  
 Já uma que retorna um valor:
 `double pegaMedia(){`
	 `return somaAvaliacao/totalAvaliacao;`
 `}`