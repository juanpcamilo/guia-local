Guia de Locais e Eventos de São Paulo: Museu do Pacaembu 

Tipografia 

Modo Responsivo 

Título da home (índex.html) (.hero h1): clamp1.75rem,1.2rem, +  2.55vw,3rem)  ~360px: 28px | ~1280px: 48px	 

Título do local (datalhe.html) - (.masthead h1): clamp(1.375rem, 1.1rem + 1.5vw, 2rem) ~360px: 23px | ~1280px: 32px. 

Mídia 

A regra img { max-width: 100%; height: auto } já estava em folha única, assim nenhuma imagem passa da largura da tela. A foto do museu estava com largura fixa de 300px e permanecia pequena no desktop. Dessa maneira, eu fiz uma mudança por width: mSin(100%, 600px) e coloquei aspect-ratio: 3 / 2 com object-fit: cover, para a foto manter a dimensão sem distorcer. Por outro lado, eu coloquei width height no <img>. Por fim, no dispositivo Galaxy A55 (360px) a foto ocupa a largura do cartão e não há rolagem horizontal. 

Usuário (toque e foco) 	 

Ambas as páginas já estavam com a meta viewport. Os dois links dos menus eram abaixo de 44px de altura e alguns não tinham um foco aparente. Arrumei com min-height: 44px dos links (menus, links dos cards, contato e rodapé) e a:focus-visible como contorno azul (branco nos fundos pretos). Já no Galaxy A55 (360px), os links facilitaram a acessibilidade do toque, o foco aparece ao navegar com o Tab e não tem rolamento na horizontal. 

Auditoria (Lighthouse, Acessibilidade) 

Página 

Nota antes 

 Nota depois 

Home 

100  

100 

Local 

98 

100 

Achado: o Lighthouse apareceu "Document does not have a main landmark" na página do local (detalhe.html). Pois, não havia uma tag <main>, então o leitor de tela não conseguia detectar o conteúdo principal. Assim, arrumei incluindo as seções, do "Sobre o local" até "Contato e links", em um <main>. A nota de acessibilidade aumentou de 98 para 100. 

Folha única × página 

 

 

 

Página 

Folha Única Resolveu Sozinha 

 

          Precisou de correção própria 

 

Home 

Reset (box-sizing), fonte, cores, img { max-width: 100% }, a:focus-visible, breakpoint de 45em. 

clamp do .hero h1, altura de toque dos links do menu, da lateral e dos cards, arial-label dos <nav>.  

 

Local 

Reset, fonte, cores, cards, tabela que vira blocos no celular, a:focus-visible. 

clamp do .masthead h1, caixa da foto (aspect-ratio e object-fit), a alteração do toque dos links do .subnav, contato, rodapé, <main> (apenas a página do local não havia). 

