# NProgressLoader #

 - User control com funcionalidade de loader para aplicações Genéxus SPA(Single Page Application) progredindo o carregamento de acordo com as etapas das requisições)
 - Barra minimalista no topo da tela
 - Loader animado centralizado na tela

# Implantação #

  - Adicione o user control ucNProgress na masterpage.
  - Na opção loader Type você define qual loader será utilizado(ProgressBar, ScreenLoader ou ambos).
  - Na opção loader Config adicione a váriavel baseada no SDT sdtNProgressConfigs.
  - O sdtNProgressConfigs é dividido em 3 níveis, Configurações Gerais, ProgressBar e Screen Loader(Especificadas nos próximos tópicos).
  - Para fazer alterações específicas nos loaders, alimente o sdtNProgressConfigs como preferir.


# Confirações Gerais #

  - loaderColor
	-> Define a cor dos loaders em hexadecimal
	(e.g: '#9925be')

# Configurações do ProgressBar #

  - minimum
        ->Muda a porcentagem mínima usada no start. (default: 0.08);
        {e.g: minimum: 0.1 }

  - template
	->Muda o template de marcação, para manter a progress bar funcionando, mantenha um elemento com a role='bar', veja o template padrão como referência
	
  {e.g: template:"<div class='....'>...</div>"}

  - easing and speed
	->Ajusta as configuraçãoes de animação usando a propriedade 'easing' do css e speed(em ms). default: ease e 200
	
  { e.g: easing: 'ease', speed: 500 }

  - trickle
	->Desliga o comportamento de autoincremento do nProgress por default essa opção vem como true. (default: true)
	
  {e.g: trickle: false }

   - trickleSpeed
	->Ajusta a frequência do autoincremento do trickle, em ms
	
  {e.g: trickleSpeed: 200 }

   - showSpinner
	->Desliga o spinner no final da barra de progresso. (default:true)
	
  {e.g: showSpinner: false }

   - parent
	-Especifica o container pai(poder default é body)
	
  {e.g: parent: '#container' });



# Configurações do Loader #

   - loaderStyle
	-> Define o estilo do loader dentre os disponíveis:(default: 4)
	0 - GRADIENT     1 - DISCO      2 - DISCO DUPLO      3 - PULSOS       4 - CUBO       5 - MODERNO
   - loaderSize
	-> Define o tamanho da div do loader em píxeis(default: 100px;)
