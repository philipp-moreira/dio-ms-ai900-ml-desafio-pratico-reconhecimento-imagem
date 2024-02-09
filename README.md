## Objetivo
Repositório contendo roteiro passo-a-passo para utilizar o Azure Vision Studio para análises de imagens.
- Análise de identificação de face
- Análise de leitura de texto em uma imagem
- Análise de adição de título/descrição à uma imagem

## Resumo
Utilizando o serviço da switch de recursos AI para lidar com imagens [**Vision Studio**](https://portal.vision.cognitive.azure.com)
será demonstrado e experimentado alguns dos recursos para lidar com processo de IA para imagens.

## Pré-requisito

### I - Possuir uma conta criada e funcional na [Azure](https://portal.azure.com/?quickstart=True#home).

Como criar a sua conta (gratuíta) ?<br>

  01 - Acesse a [página](https://azure.microsoft.com/pt-br/free/search/?ef_id=_k_CjwKCAiA8YyuBhBSEiwA5R3-EyxckFGkfk85I8455z8A8V9SEQ4rDamiBh29pzPeSy5ADC1geYuP7hoCVIAQAvD_BwE_k_&OCID=AIDcmmzmnb0182_SEM__k_CjwKCAiA8YyuBhBSEiwA5R3-EyxckFGkfk85I8455z8A8V9SEQ4rDamiBh29pzPeSy5ADC1geYuP7hoCVIAQAvD_BwE_k_&gad_source=1&gclid=CjwKCAiA8YyuBhBSEiwA5R3-EyxckFGkfk85I8455z8A8V9SEQ4rDamiBh29pzPeSy5ADC1geYuP7hoCVIAQAvD_BwE)

  02 - Clique em **Experimente gratuitamente**
![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/08bfb1e9-14d1-43a4-bcb4-61c64b24c900)

  03 - Você será redirecionado para [página\(abaixo\)](https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize?client_id=8e0e8db5-b713-4e91-98e6-470fed0aa4c2&response_type=code%20id_token&scope=openid%20profile&state=OpenIdConnect.AuthenticationProperties%3DtgIM8fUAqWeFNuvBd5GgL10awhlqhovrf_LeaF_V98VPjWvVVvh2l9wKa-TrmbYJkc5Qc0FyajfyI5oeDXhqUK3jq3J9KPIMVyBIqbDpKgLZ9OiladetOb9xfipP-LuLXa1ZvHmnx5VVmbWufDcTnUHnKZi842K2G2KMO3NoPmdYptG07X_VQuMEe0PBVLCv4wCg2402VAfBdrlkj4Zmj4XlXttNbbzLpEVUazwaUiF7pyLsphYwL6yukZglxfwmOrsLM143q55SR8rcde7Bl7onUiPYDMnODPWXibG8KhX8es6YLk-ETzUhQevJ4iSOmkpXRr9eC6r05WWRMe79zP-7qtfuuNcjcRQ3gBoehTjy92nVEImQBeFUueuTwuRBzIcwmLamlq0q7rlaNfYxhlR3HdRkTLu9J5kIWVxLi_7cuo9jG0sZgxJkSU9E3l67t7eI-HwiwGcLqkgFyNeKzGFYJ8SOC6luw27lLZ9KJ2XOWWWsZCsMpHJNaRPZna-kscK7tQRLAbJF-TH2OAOJoeypVbeWkvvS9yDOz6lORRrTvjTiBDC61jAZN0ZVXBhgw0sA61h8CO4ikIG_dMASZfC73qW12-u6QuLOoIHODOgmBxPsbzLT2cwTagbMufnr14hY4Dw2J1YomUKAE400RYrUxloEbh5xwZ5ifFSUuVLeixYtnON7bckL9eDqJ9CDc60xdnRF6HvFSWA_FxoK3zWCAxkF6z6FT8XJ068z8RWK0EpCZhKvhB-nKPsitDminmf5nwgdkY6m01Mnv7EAvZD4-OMzAND_14gNhN8B--nZrqKE1GEqiKfupkUtQWf94y7tXzlmBSEGe2uCBdmZkVe2UN9jxLR7ZRMzWGsVyKU5K3Ibw-HGcYaZDctMXRFrDaJF5N6OaN9tiTQ279Qb5PdNsb6nK0W2JrAgZkMo6txZIXhjQ1Z3r57W-vwU7AvpYNB4p9E3b17v-7LPZ_5QJILZaJZ_s_sf1mHh62hAINGfEpsuZKDrQ9-9rILdKX1JQiQlYietTOmKzF3bHk747LYWqtRy5sOayt1fyQgF5IvfiDVMz2KOsnOZGBH1R1FNTBKKZLt8fPDXw01sWsnsByhbmSuWTAQoRSWPJOy_gLx-tFBCI0DrTx2mFp_JuopusiE0J6bBm-coigEQBfUa57k-3endmqockVvi1892dPxvUHSS3pE4Bv8aB0nhq5s1pMjaCTVRosZncZfwkpapUg-joaWGaJ1xoO_rxXXocrjdaMKC3ko0l7YGhuCSmbr2-5pjITW6MmUBOdX0kymnpGNVWiTXC75a3d9UlKQOBe_z3Z9gPhHayCZDlMqzttja8ehvRid36s08fAf9er5Wz4As6NZgXBYfY1YXe4mWEn9PBcf7Tzya1c76qNIPlgj5LwqMqwOZDUUrbjooTRbrKg&response_mode=form_post&nonce=638429565329591794.NjVhYzg0ZjItM2U0My00MDY1LWEyODAtMzI3ZjZkNzQ5YmI4ZDgxNzA2NWYtODhmZS00MGQ2LTkxZWQtNGQ4ZDJmOTY1NTgy&redirect_uri=https%3A%2F%2Fsignup.azure.com%2Fapi%2Fuser%2Flogin&max_age=86400&post_logout_redirect_uri=https%3A%2F%2Fsignup.azure.com%2Fsignup%3Foffer%3Dms-azr-0044p%26appId%3D102%26ref%3D%26redirectURL%3Dhttps%3A%2F%2Fazure.microsoft.com%2Fget-started%2Fwelcome-to-azure%2F%26l%3Dpt-br%26srcurl%3Dhttps%3A%2F%2Fazure.microsoft.com%2Ffree%2Fsearch%2F%3Fef_id%3D_k_cjwkcaia8yyubhbseiwa5r3-eyxckfgkfk85i8455z8a8v9seq4rdamibh29pzpesy5adc1geyup7hocviaqavd_bwe_k_%26ocid%3Daidcmmzmnb0182_sem__k_cjwkcaia8yyubhbseiwa5r3-eyxckfgkfk85i8455z8a8v9seq4rdamibh29pzpesy5adc1geyup7hocviaqavd_bwe_k_%26gad_source%3D1%26gclid%3Dcjwkcaia8yyubhbseiwa5r3-eyxckfgkfk85i8455z8a8v9seq4rdamibh29pzpesy5adc1geyup7hocviaqavd_bwe&x-client-SKU=ID_NET472&x-client-ver=6.34.0.0), onde você vai ter as opções de loggin utilizando:

  - Sua conta de e-mail microsoft/outlook
  - Sua conta github

  Selecione a opção desejada e prossiga com seu login.
![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/40758dd3-93bc-46ee-ab6d-839ca04f62ac)

  04 - Logo após a autenticaçào, você vai visualizar duas opções, onde a primeira pede sua confirmação (marcando o checkbox) para o termos de planos do Azure e o segundo pede sua confirmação se deseja permitir à Microsoft compartilhar seu e-mail com parceiros comerciais e que provem produtos via plataforma da Azure, este segundo não é um item obrigatório, assim, fica a seu critério de como deseja seguir;

  05 - Mais abaixo dos dois checkbox citados no passo anterior, você irá visualizar o campo para selecionar ou cadastrar um cartão de crédito, no qual será feito a cobrança\*<br>
  Clique em "Criar Conta" e prossiga.
_\***Cobrança**: Com a conta gratuita você irá receber um bonus da Microsoft Azure +/- no valor de $ 200,00 e caso este saldo seja totalmente consumido pelos seus recursos criados o valor sobressalente será debitado no cartão cadastrado e selecionado._

  06 - Sua conta e cadastro serão criado e você deve ser redirecionado para Painel de gestão dos seus recursos Azure, como demontrado abaixo.
  No caso como esta conta é uma conta gratuita e com propósito de aprendizagem não possuo nenhum recurso criado.
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico/assets/17642499/9d9ddacd-c202-4881-a8e4-1a35727e2151)

  
## Passo-a-Passo

### Análise de identificação de face
  1 - Ao acessar o Vision Studio e após definir o recurso do Azure Service IA como padrão
  
  2 - Clique em [Face]
  
  3 - Clique em [Detect faces in an image]
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico-reconhecimento-imagem/assets/17642499/b063aee9-398f-4a5c-9a03-18d279781c34)
  
  4 - Utilize uma das imagens de amostra ou carregue uma imagem própria

  Após a imagem carregada o serviço instantaneamente inicia análise visando identificar um rosto humano e após detectar realiza o mapeamento da imagem mapeando as coordenadas de cada parte do rosto identificada, carregando todo esse mapeamento em uma resposta formatada como JSON.
  
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico-reconhecimento-imagem/assets/17642499/2a204de0-a9b5-4b0b-b687-edb864126178)
  
### Análise de leitura de texto em uma imagem
  1 - Ao acessar o Vision Studio e após definir o recurso do Azure Service IA como padrão
  
  2 - Clique em [Optical character recognition]
  
  3 - Clique em [Extract text from images]
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico-reconhecimento-imagem/assets/17642499/8fd8d4ff-9dfb-4660-83a7-515227a01cf8)

  4 - Utilize uma das imagens de amostra ou carregue uma imagem própria

  Após a imagem carregada o serviço instantaneamente inicia análise visando identificar o(s) texto(s) contidos na imagem e após detectar realiza o mapeamento do(s) texto(s) transcrevendo o resultado.
  Neste exemplo utilizei uma foto com escrita cursiva e ele chegou muito próximo ao resultado de 100%, porquê, se oservado a imagem e o resutlado mapeado utilizei na imagem uma sepração de linha que consiste de linhas onduladas mais duas barras para frente, porém, o serviço reconheceu como sendo algarismo numérico 1.

  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico-reconhecimento-imagem/assets/17642499/e4e5de0b-1a07-4a28-9f0e-66fa947d212c)

### Análise de adição de título/descrição à uma imagem

  1 - Ao acessar o Vision Studio e após definir o recurso do Azure Service IA como padrão
  
  2 - Clique em [Image Analysis]
  
  3 - Clique em [Add captions to images]
  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico-reconhecimento-imagem/assets/17642499/11810150-aa46-4117-96a4-6572219bcd16)

  4 - Utilize uma das imagens de amostra ou carregue uma imagem própria

  Após a imagem carregada o serviço instantaneamente inicia análise visando obter uma descrição que descreva a imagem em forma textual. 
  Ao observar o resultado retornado pelo serviço considerei satisfatório, mas, não perfeito, pois creio que o resultado poderia ser mais detalhado, por exemplo, relatando tipo de pão, recheio do sandwich.

  ![image](https://github.com/philipp-moreira/dio-ms-ai900-ml-desafio-pratico-reconhecimento-imagem/assets/17642499/601acfb5-fc1e-47c0-be8b-bad54a43ee23)
