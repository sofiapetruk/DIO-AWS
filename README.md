# DIO-AWS

Computação da Nuvem com EC2

Amazon EC2
O que são Instâncias EC2

	EC2 (Elastic Compute Cloud) - São máquinas virtuais na AWS, podendo ser com sistema operacional Windows ou Linux.

	Pense no EC2 como a versão digital de um computador físico. Em vez de comprar um servidor caro, se preocupar com a manutenção, com a refrigeração e com a energia, você simplesmente “aluga” um computador virtual da AWS. Esse computador virtual chamado de instâncias, vem com processador, memória, armazenamento e um rede virtual para você usar como quiser.

Uma EC2 é composta por:
CPU
Memória
Disco
Rede
Sistema
Operacional
No modelo Cloud, uma EC2 é do tipo IAAS, ou seja, quando criamos um EC2 estamos utilizando o tipo Infraestrutura como serviço.

E qual seria nossa responsabilidade sobre este recurso?
Seria dos aplicativos, dados e conexões que fazemos.

Como escolher a EC2 correta para minha aplicação?
Escolher a instância correta na AWS é crucial para garantir eficiência, escalabilidade e economia nos gastos com nuvem.
Vamos explorar como o Amazon EC2 pode atender às necessidades específicas de sua aplicação.
Escolher a instância certa não se trata apenas de selecionar um tipo aleatório, mas sim de entender as necessidades da sua aplicação e utilizar os recursos da nuvem de forma inteligente para alcançar eficiência operacional e econômica.

EC2 - Terminologia
O Amazon Elastic Compute Cloud (EC2) nos fornece a capacidade de computação na cloud da AWS.
As imagens de máquina da Amazon estão disponíveis para escolha no momento da criação.
Pode definir a segurança básica utilizando firewall incorporado do AWS, utilizar grupo de segurança, protocolo, porta, IPs de origem que permite ou nega o acesso às suas instâncias EC2.
Como funciona?
	A grande vantagem do EC2 é a sua elasticidade, que é o “E” de Elastic no nome do serviço. Essa característica permite que você aumente ou diminua os recursos do seu servidor de forma rápida e automática, dependendo da necessidade da sua aplicação.
Escolha do “hardware”: Primeiro, você escolhe o tipo de instância que melhor se adapta à sua necessidade. Existem centenas de tipos de instâncias como foco em processamento (CPU), memória, armazenamento ou até mesmo com placas de vídeo (GPUs) para tarefas de machine learning.

Configuração do software: Depois de escolher o hardware, você seleciona a Amazon Machine Image (AMI), que é um modelo de software que já vem com um sistema operacional pré-instalado (como Linux ou Windows), e, opcionalmente, com alguns softwares adicionais. É como escolher o sistema operacional que você quer instalar no seu computador.

Lançamento da instância: Com o hardware e o software selecionados, você lança a sua instância. Em poucos minutos, seu servidor virtual estará pronto para você.

Gerenciamento e escalabilidade: Você pode se conectar à sua instância remotamente para instalar o seu software, rodar a sua aplicação, configurar bancos de dados, etc. O EC2 também oferece ferramentas para que você possa aumentar ou diminuir o número de instâncias automaticamente. Se eu tiver um pico de tráfego o EC2 pode criar novas instâncias para lidar com a demanda e depois desligá-las quando o tráfego diminuir, economizando dinheiro.

Modelo de pagamento: Com o EC2, você paga apenas pelo que usa, geralmente por segundo de uso. Isso elimina a necessidade de grandes investimentos iniciais em hardware e permite que você tenha um controle muito maior sobre os seus custos.


Tipos de Instâncias EC2

Família de Instância
Principais Características
Casos de Uso Comuns
Uso Geral (T e M)
Equilíbrio entre CPU, memória e rede.
Servidores web, ambientes de desenvolvimento e teste, aplicações de pequeno e médio porte.
Otimizadas para Computação (C)
Alta performance de CPU e alta frequência de processador.
Servidores web de alta performance, computação de alto desempenho (HPC), codificação de vídeo.
Otimizadas para Memória (R, X e Z)
Grande quantidade de memória RAM em relação à CPU.
Bancos de dados in-memory, bancos de dados relacionais grandes, análise de Big Data.
Computação Acelerada (P, G, Inf e Trn)
Uso de hardware especializado com GPUs (P e G) e chips da AWS (Inf e Trn).
Machine learning, inteligência artificial (IA), processamento de gráficos, computação científica.
Otimizadas para Armazenamento (I e D)
Grande capacidade de armazenamento local, rápido e de alta performance.
Bancos de dados NoSQL, data warehouses, sistemas de arquivos distribuídos.




Otimização de Recursos
	Quando falamos em otimização de recursos, estamos apontando para “custo”, ou seja, otimizar recurso é poupar custos na AWS.
	Mesmo otimizando um recurso computacional, onde melhoramos o desempenho do sistema, estamos poupando custo, pois isto traz ganho para a nossa solução na nuvem.
Desligando instâncias não utilizadas
Em ambientes produtivos não há a necessidade, mas em ambientes como de desenvolvimento, testes, treinamento, geralmente não são utilizados nos períodos noturno ou finais de semana e podem ser desligados.
Uma menor utilização implica diretamente em economia de custos.

Remover recursos ociosos ou não utilizados
É comum criarmos recursos e não verificar a utilização e ficarmos com vários recursos ociosos no ambiente. Isto gera gastos, recursos ociosos, parados em nosso ambiente gera gasto.
Seria como alugar um carro e deixar na garagem!

Escalar recursos
Nós executamos o scale de recursos para processar os workloads em determinados momentos. Temos a opção de aumentar ou diminuir de forma manual ou automática.
Vertical vs Horizontal 
Escalando Verticalmente
Significa acrescentar ou reduzir capacidade de um recurso em um mesmo nó e geralmente está relacionado a alterar o número de vCPUs, memória, storage, rede de uma instância.
Com isso, otimizamos o custo através de escalabilidade vertical aumentando recursos somente para lidar com um pico de consumo e reduzi-los conforme a diminuição da demanda.

Escalando Horizontalmente
É quando você aumenta o número de recursos. Por exemplo, adicionando mais um disco rígido, adicionando mais uma instância para suportar a aplicação.
Com isso, otimizamos o custo através de escalabilidade vertical aumentando recursos somente para lidar com um pico de consumo e reduzi-los conforme a diminuição da demanda.
Sob Demanda
As instâncias on-demand são compradas a uma taxa fixa por hora e são recomendadas para aplicativos com cargas de trabalho irregulares de curto prazo que não podem ser interrompidas. Elas também são adequadas para uso durante o teste e desenvolvimento de aplicativos no EC2.

Instâncias Reservadas
Costumam ser mais baratas que as instâncias sob demanda, mas você precisa pagar o ano inteiro de uso. É uma desvantagem para quem não precisa usar a instância com frequência.

Instâncias SPOT
Garante a disponibilidade das aplicações sob demanda com descontos de até 90%. A desvantagem das instâncias SPOT é que elas podem ser encerradas pela Amazon Web Service (AWS) a qualquer momento, com um aviso de dois minutos.

Armazenamento na Nuvem com Amazon EBS e S3
Amazon EBS
   Elastic Block Store (EBS), nada mais é do que uma storage altamente confiável que pode ser anexada em qualquer instância EC2. Toda instância possui um volume de armazenamento.

Agora com o EBS conseguimos ter a capacidade de expansão de forma rápida, com apenas alguns clicks.
Então como o EBS conseguiu criar uma nova partição em nossa instância, seria como anexar um HD externo. Escolhemos o modelo e o size e anexamos a nossa VM.

Exemplos de uso:
Armazenamento para banco de dados, como MySQL, PostgreSQL e Oracle.
Armazenar dados para aplicativos web e logs de sistema.





Amazon S3
  Amazon S3 (Amazon Simple Storage Service) é um serviços de armazenamentos de objetos em nuvem oferecidos pela AWS.
   É ideal para armazenar, organizar e recuperar grandes volumes de dados de forma segura e escalável.
O Amazon S3 possui algumas classes de storages onde conseguimos economizar os custos.
Um exemplo muito bom para entendermos as diferentes classes do S3 é o exemplo do exame de Hospital.





    https://aws.amazon.com/pt/s3/storage-classes/





	 Podemos utilizar regras do ciclo de vida para definir a forma como o Amazon S3 gere os objetos durante o seu tempo de vida.
	O Lifecycle permite fazer a transição de objetos e migrar automaticamente para a classe Glacier.




