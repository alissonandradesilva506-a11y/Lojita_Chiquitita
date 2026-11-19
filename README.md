# Lojita_Chiquitita
O objetivo dessa tarefa foi criar um catálogo de itens com uma combinação de vários módulos de bancos de dado.

A interface do catálogo foi feito com o Python do Google Colab através de Gradio, combinando os melhores atributos de Supabase, MongoDB e Redis para realizar funções importantes do catálogo.

Supabase foi utilizado para realizar o cadastro do admin através da tabela 'credenciais', providenciado o 'email' e 'senha' do sistema e as utilizando na função 'autenticar_admin'

MongoDB foi utilizado para guardar os itens em si e cadastrar novas adições através das funções  

Redis serve para atualizar a página de catálogo, adicionando os itens mais novos com lrange, lrem, lpush e ltrim nas funções 'obter_recentes' e 'registrar_visto_recentemente'.

# Instruções
Quando o app começa o catálogo de itens é imediatamente visível, um botão na parte de cima da página troca a visão dos clientes para a versão do admin. 

Na página do admin o sistema pede pelas credenciais. Se colocadas a página inteira é desbloqueada, revelando a função de cadastrar novos itens, o sistema pede o nome, preço, descrição, categoria e o link da imagem do item. Quando todos os aspectos estão preenchidos o botão de cadastro fica disponível para clicar e automaticamente adiciona esse item no catálogo.

Na página do cliente o sistema mostra o catálogo como foi mencionado anteriormente, mas a sua função principal é o carrinho que serve para guardar a ordem de itens de um pedido hipotético. O cliente escolhe o produto que deseja colocar junto com a sua quantidade e o app não só adiciona ele no carrinho atual, mas também calcula o total de todos os itens. Por fim, quando o cliente termina de escolher ele pode clicar no botão de 'Finalizar compra no Whatsapp' para enviar uma mensagem no Whatsapp do cliente enviando a conta total e perguntando se ele deseja comprar mesmo os itens escolhidos.
