# Cargos_TCE_PB
<p>Scripts em python para cria&ccedil;&atilde;o de base de dados local dos cargos de servidores municipais e estaduais fornecidos pelo Tribunal de Contas do Estado da Para&iacute;ba(TCE-PB) e consulta de tais informa&ccedil;&otilde;es. Foi tamb&eacute;m adicionado um script em php para visualiza&ccedil;&atilde;o dos dados, que poder&aacute; ser acessado pela instala&ccedil;&atilde;o de miniservidores, sugerindo-se XAMPP.</p>
<p>Tais dados podem ser salvos em uma planilha excel.</p>
<p><b>Obs: Em 21.06.2017, o TCE disponibilizou a remuneração dos servidores e retirou a numeração completa do CPF. Assim, o campo do CPF equivale aos 6 dígitos do meios. Ex: o CPF ###.123.456-##. está no formato 123456</b></p>

<p style="margin-bottom: 0cm; line-height: 100%;" align="left"><br /> Os dados est&atilde;o dispon&iacute;veis no site dados.tce.pb.gov.br.</p>
<p style="margin-bottom: 0cm; line-height: 100%;" align="left">A base de dados &eacute; montada com full text search(fts3 com tokenizer unicode61) em sqlite3. Isso quer dizer que:</p>
<p style="margin-bottom: 0cm; line-height: 100%;" align="left">1. Acentos s&atilde;o ignorados</p>
<p style="margin-bottom: 0cm; line-height: 100%;" align="left">2. Mais&uacute;culo/min&uacute;sculo &eacute; ignorado</p>
<p style="margin-bottom: 0cm; line-height: 100%;" align="left">3. Operadores podem ser utilizados. A exemplo de * ? OR NEAR NOT.</p>
<p style="margin-bottom: 0cm; line-height: 100%;" align="left"><br /> <br /> Para mais informa&ccedil;&otilde;es, vide: http://www.sqlite.org/fts3.html<br /> <br /> <strong>Aten&ccedil;&atilde;o!Antes de tudo:<br /> </strong>a) Verifique se voc&ecirc; possui pelo menos 12gb de espa&ccedil;o em seu HD<br /> b) Se estiver utilizando command prompt e um proxy, vc dever&aacute; configur&aacute;-lo digitando: SET HTTP_PROXY=http://login.senha@proxy:porta<br />c) O script foi projetado para windows. Se voc&ecirc; utilizar linux voc&ecirc; tem condi&ccedil;&otilde;es de adapt&aacute;-lo para suas necessidades :)<br /> <br /> <span style="font-size: large;"><strong>Como criar a base de dados:<br /> </strong></span>1. Instale python anaconda em: https://www.continuum.io/downloads<br /> Em caso de d&uacute;vidas, opte pela vers&atilde;o 32bits.<br /> 2. Baixe o reposit&oacute;rio no canto superior direito (Clone or download)<br /> 3. No prompt de comando digite: <br /> pip install supersqlite<br /> 3. Execute o script criador_base_dados.py. Ele baixar&aacute; os arquivos do site dados.tce.pb.gov.br e iniciar&aacute; a cria&ccedil;&atilde;o da base de dados folhapessoal.db.<br />  Depois, v&aacute; na pasta do usu&aacute;rio -&gt; anaconda 3 -&gt; Selecione python.exe<br /> Ele poder&aacute; falhar. Clique duas vezes novamente e vai funcionar.<br /> A cria&ccedil;&atilde;o da base de dados varia conforme computador, mas deve demorar cerca de uma hora<br /><br /> <span style="font-size: large;"><strong>Como consultar em Python</strong></span></p>

<p style="margin-bottom: 0cm; line-height: 100%;" align="left"><span style="font-size: large;"><strong>Como consultar em&nbsp;PHP</strong></span></p>
<p style="margin-bottom: 0cm; line-height: 100%;" align="left">Instale um miniservidor. Em windows, uma solu&ccedil;&atilde;o f&aacute;cil &eacute;&nbsp;<a href="https://www.apachefriends.org/pt_br/index.html">XAMPP</a>&nbsp;. Depois, copie a pasta para o diret&oacute;rio utilizado pelo XAMPP (normalmente &eacute; C:\xampp\htdocs). Depois, inicie o XAMPP. Abra o&nbsp;seu browser e acesse o script (normalmente &eacute;&nbsp;<a href="http://localhost/CARGOS_TCE/cargos_tce.php">http://localhost/CARGOS_TCE/cargos_tce.php</a>)</p>
