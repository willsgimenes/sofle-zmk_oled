ZMK CONFIG


Primeiro de tudo no caso de teclados mais utilizados, como Sofle, Lily58, Corne e alguns outros, é interessante começar pelo site do ZMK.
https://zmk.dev/docs/user-setup ->
![image](https://github.com/user-attachments/assets/07776e9f-de8b-4a12-ba79-470632582f6d)

Primeiro passo é forkar a config setup do ZMK.
Escolher a board do seu teclado, que na maioria das vezes será 
Board:Nicenano V2
Escolher o seu teclado e copiar o layout base/default para o github.
![image](https://github.com/user-attachments/assets/0527c640-3f06-4531-b0c0-1f64584daef7)

É importante fazer essa configuração inicial, para que então você consiga alterar o keymap da melhor forma.

Existem 3 formas de alterar o layout pelo ZMK.

 1. Diretão pelo ZMK, no github ->
![image](https://github.com/user-attachments/assets/3cc4374a-771b-4393-8859-d5db8fbc1b11)

Para fazer as alterações pelo github, é só alterar e criar regras no teclado.keymap de acordo com o que você o USER achar melhor, diretão pelo zmk é o melhor quando você já leu as docs do zmk e sabe exatamente o que está fazendo!
Aqui, nunca vai ter algum tipo de limitação por GUI, apenas limitação pelo seu próprio código.

  Para configurar o teclado pela 1 e 2 forma, é necessário sempre que fazer uma alteração na configuração do teclado,
  Compilar pelo actions
![image](https://github.com/user-attachments/assets/39f41191-e2d7-4da3-bccc-ba8f2fe95532)
  Após a primeira compilação pelo actions, sempre que fizer uma alteração em alguma das pastas do zmk, o actions vai compilar automaticamente.
  
  Após compilar o actions, se a alteração for bem sucedidade gerará um arquivo de firmware - >
  ![image](https://github.com/user-attachments/assets/1becced2-b136-44bc-a42f-6060e3e2a36d)

  Após baixar o arquivo de firmware e descompilar, provavelmente haverá gerado dois ou três arquivos.
  ![image](https://github.com/user-attachments/assets/385dad17-e6ec-4ec7-9e66-682085ad602f)
  
  Keyboard.left.uf2 
  
  Keyboard.right.uf2
  
  Settings.reset ( esse é utilizado apenas em casos especificos )

  Por fim, para flashear o firmware novo é só dar dois cliques no botão de RST do teclado em menos de 1s, e abrirá uma pasta, igual um pendrive com o nome de "Nicenano"
 ![telegram-cloud-photo-size-1-5040021887542996513-y](https://github.com/user-attachments/assets/217fe770-6b37-4470-a5f0-d6640a593a94)

  e é só jogar o arquivo LEFT, no teclado esquerdo.
  E jogar o arquivo RIGHT, no teclado direito.

  Nunca é preciso apagar nenhum arquivo dentro do Nicenano ( ou outra MCU ), sempre que atualizar só é necessário jogar um arquivo novo.

  ![image](https://github.com/user-attachments/assets/fec189f3-8293-4407-89ad-9f4268b701dc)
   
    É comum que apareça um erro após após passar o novo firmware pra o teclado. Fiquem tranquilos não é um bug, é um feature do zmk : )


2. Pelo KeymapEditor {https://nickcoutsos.github.io/keymap-editor/} ->
![image](https://github.com/user-attachments/assets/1bffa913-4f2e-4369-be6f-9c86814e70db)

Este é BY FAR o que eu mais recomendo para quem está iniciando, é uma GUI sem limitações, você pode configurar de tudo e ainda aprender enquanto configura, tap dance, behaviours, conditional layers, macro, combo,  layers infinitas e etc.
O Keymap Editor é especial porque basicamente automatiza as alterações que foram feitas na GUI de volta para o github e também builda o actions automaticamente.


![image](https://github.com/user-attachments/assets/c7c339a6-d595-4469-b02d-d556a2a272ed)


3. ZMK STUDIO -> Esse é a GUI mais nova do ZMK, ainda está em Beta, tem algumas limtações, não gosto de recomendar pois não salva as configs do ZMK direto no github, além de não ter algumas configurações de tap dance e behaviours.
![image](https://github.com/user-attachments/assets/f1532b9f-3dba-42ea-84fa-412ed3341d09)

A vantagem do ZMK.STUDIO é que você quase nunca precisará mexer em código, compilar, baixar e passar o novo firmware de cada alteração, para o teclado, o que pode definitivamente ser chato. Mas, tbh, não acho que vale a pena, ao menos quando você ainda está
aprendendo a usar o ZMK.
