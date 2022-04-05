# Limbus Network. (LN128)

- Limbus Network é um método de contato não centralizado, e cada computador que roda o software é um nó (ou node) desta rede, e funciona como um servidor próprio.


# private and public keys (1/2)

- O limbus_main.js admnistra os processos e o key_creator.js gera outros dois arquivos, a criptografia de chave pública usa um par de chaves relacionadas matematicamente (private_key.pgp, public_key.pgp). Uma mensagem criptografada com a primeira chave deve ser decriptografada com a segunda chave e uma mensagem criptografada com a segunda chave deve ser decriptografada com a primeira chave.
Cada participante em um sistema de chave pública possui um par de chaves. Uma chave é nomeada como a chave privada e é mantida secreta. A outra chave é distribuída para quem deseja recebê-la; essa chave é a chave pública.
Qualquer um pode criptografar uma mensagem usando sua chave pública, mas somente você pode lê-la. Ao receber a mensagem, decriptografe-a usando sua chave privada.

- O método usado é openPGP.

- A cada 50 minutos uma nova chave é criada pelo key_creator.js e substituida automaticamente. Vai de sua escolha deletar as antigas chaves ou não, caso tenha alguma mensagem não decriptada.


# Advanced Encryption Standard, AES128 (2/2)

- A estrutura usada é rede de substituição-permutação com 128 blocos de bits, mesmo com um supercomputador, levaria 1 bilhão de bilhões de anos para quebrar a chave AES de 128 bits usando um ataque de força bruta. Isso é mais do que a idade do universo.


# Limbus Routing (ONION)

- Por cada computador ser um nó, ao usar e concordar com a conexão, seu computador "escolhe" inumeras relays para encaminharem seu tráfego de forma que ele saia fracionado por vários últimos IP's (relays de saída.) e com isso se torna impossivel saber da onde veio a mensagem, entretanto é possivel saber o target pelo smart contract.


# Uso de dados.

- Cada computador realizará micro compartilhamentos de dados, ou seja, pelo processo de fracionar sua data em packages é reduzido significamente a carga das redes individuais. Mesmo que um nó intercepte e tenha a chave privada para a decriptação, o mesmo seria imposssivel pois está faltando partes.
 
- Após a mensagem ser montada e decriptada por sua chave privada, ao decorrer de 20 minutos a deleção acontece, incapaz de ser recuperada por métodos forenses.

<img src="https://github.com/obrientatsuya/Limbus-Network-LN128-/blob/main/limbusnetworkrouting.png?raw=true"/>

- EX: receberás a fração de um dado criptografado(500kb) que após continuar o fluxo randomico, será deletado.

# Smart Contract 
O que é Smart Contract? É uma condição imposta que, uma vez alcançada, executa automaticamente uma determinada função. Será usado para garantir a segurança e compartilhamento dos dados, evitando problema de alterações e perca de pacotes na etapa de Routing. 6 Grandes condições, 1 - Definição de Target, 2 - Limite de tamanho, 3 - Permitido apenas AES128, 4 - Decisão randomica e fração de pacotes, 5 - Ordem para montar, 6 - Contrato confirmado entre dois nós. Só depois de tudo isso é possivel enviar os pacotes.

