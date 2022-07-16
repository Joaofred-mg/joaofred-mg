### Oie devs 👋

Sou João Frederico Fernandes Ludolf, apaixonado por tecnologia, gosto de criar ótimos softwares, amo games  e sou extremamente apaixonado pelo universo tech estou aprofundando meu conhecimento a cada dia mais e buscando ser um melhor DEV para poder ser uma inspiração e poder ensinar o que eu sei também.


<img align="right" width="300" src="https://i2.wp.com/allhtaccess.info/wp-content/uploads/2018/03/programming.gif?fit=1281%2C716&ssl=1" />


## **Linguagens e Ferramentas:**  
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/visual-studio-code/visual-studio-code.png"></code>
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png"></code>
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/react/react.png"></code>
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/git/git.png"></code>
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png"></code>
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png"></code>
<code><img height="30" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/css/css.png"></code>

programa
{
	inclua biblioteca Graficos --> g
	inclua biblioteca Teclado --> t
	inclua biblioteca Util --> u

	inteiro boba = -1
	inteiro porg = -1

	inteiro porgx = 100, porgy = 100

	inteiro temp
	
	funcao inicio()
	{
		g.iniciar_modo_grafico(verdadeiro)
		g.definir_dimensoes_janela(800, 600)
		boba = g.carregar_imagem("salvar_imagem/boba.jpg")
		porg = g.carregar_imagem("salvar_imagem/porg.png")
		
		enquanto(verdadeiro){
			g.definir_cor(g.COR_BRANCO)
			g.limpar()
			g.desenhar_imagem(0, 0, boba)
			g.desenhar_imagem(porgx, porgy, porg)
			se(t.tecla_pressionada(t.TECLA_SETA_ESQUERDA)){
				porgx--
			}
			se(t.tecla_pressionada(t.TECLA_SETA_DIREITA)){
				porgx++
			}
			se(t.tecla_pressionada(t.TECLA_SETA_ACIMA)){
				porgy--
			}
			se(t.tecla_pressionada(t.TECLA_SETA_ABAIXO)){
				porgy++
			}
			se(t.tecla_pressionada(t.TECLA_P)){
				temp = g.renderizar_imagem(800, 600)
				g.definir_cor(g.COR_BRANCO)
				g.limpar()
				g.renderizar()
				g.salvar_imagem(temp, u.obter_diretorio_usuario()+"/Documents/Porgs/porg" + porgx + "_" + porgy + ".png")
				g.liberar_imagem(temp)
				g.definir_cor(g.COR_PRETO)
				g.limpar()
				g.renderizar()
			}
			g.renderizar()
		}
	
	}
}

