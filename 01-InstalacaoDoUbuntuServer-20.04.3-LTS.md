Autor: Robson Vaamonde<br>
Procedimentos em TI: http://procedimentosemti.com.br<br>
Bora para Prática: http://boraparapratica.com.br<br>
Robson Vaamonde: http://vaamonde.com.br<br>
Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
LinkedIn Robson Vaamonde: https://www.linkedin.com/in/robson-vaamonde-0b029028/<br>
Data de criação: 10/10/2021<br>
Data de atualização: 10/10/2021<br>
Versão: 0.01<br>
Testado e homologado no GNU/Linux Ubuntu Server 20.04.3 LTS

Atualização da versão do Ubuntu Server 20.04.3: https://wiki.ubuntu.com/FocalFossa/ReleaseNotes<br>
Mudanças da versão do Ubuntu Server 20.04.3: https://wiki.ubuntu.com/FocalFossa/ReleaseNotes/ChangeSummary/20.04.3<br>
Ciclo de Lançamento do Ubuntu Server: https://ubuntu.com/about/release-cycle

OBS1 - lentidão da instalação e configuração do Ubuntu Server 20.04.x no Oracle VirtualBOX<br>
Link1: https://forums.virtualbox.org/viewtopic.php?f=3&t=98944<br>
Link2: https://forums.virtualbox.org/viewtopic.php?f=7&t=98586<br>

Primeira etapa: Download da ISO do Ubuntu Server 20.04.3 LTS

01. Link de download do Ubuntu Server: https://releases.ubuntu.com/20.04.3/
02. Versão do download Ubuntu Server: ubuntu-20.04.3-live-server-amd64.iso (24/08/2021)
03. Arquitetura do Ubuntu Server: AMD64 (64-bit)
04. Tipo de instalação: DVD Image (ISO) Installer

Segunda etapa: Criação e Configuração da Máquina Virtual no Oracle VirtualBOX<br>
Link de download do Oracle VirtualBOX: https://www.virtualbox.org/wiki/Downloads

	_ 01. Ferramentas;
	_		Novo
	_ 02. Nome e Sistema Operacional:
	_		Nome: UbuntuServer-2004
	_		Pasta da Máquina: (deixar o padrão do sistema)
	_		Tipo: Linux<br>
	_		Versão: Ubuntu (64-bit)
	_	<Próximo>
	_ 03. Tamanho da memória:
	_		Tamanho: 2048MB
	_	<Próximo>
	_ 04. Disco Rígido:
	_		Criar um novo disco rígido virtual agora
	_	<Criar>
	_ 05. Tipo de arquivo de disco rígido
	_		VDI (VirtualBOX Disk Image)
	_	<Próximo>
	_ 06. Armazenamento em disco rígido físico
	_		Dinamicamente alocado
	_	<Próximo>
	_ 07. Localização e tamanho do arquivo
	_		Localização: (deixar o padrão do sistema)
	_		Tamanho do disco: 50GB
	_	<Criar>
	_ 08. Configurações da Máquina Virtual UbuntuServer-2004 (Propriedades/Configurações)
	_	Sistema
	_		Placa Mãe
	_			Recurso Estendidos
	_				Relógio da máquina retorno hora UTC: Desabilitar
	_		Processador
	_			Processadores: 02 CPUs
	_			Recursos Estendidos: Habilitar PAE/NX
	_	Monitor
	_		Tela
	_			Memória de Vídeo: 128MB
	_			Aceleração: Habilitar Aceleração 3D
	_	Áudio
	_		Habilitar Áudio: Desabilitar
	_	Rede
	_		Adaptador 1 (LAN)
	_			Habilitar Placa de Rede
	_			Conectado a: Rede Interna
	_			Nome: (deixar o padrão do sistema: intnet)
	_	<OK>

Terceira etapa: Iniciando a Instalação do Ubuntu Server 20.04.3 LTS (localizar a ISO)

	_ 01. VM UbuntuServer-2004: Iniciar
	_ 02. Selecione o disco rígido de boot
	_ 		Selecionar um arquivo de disco óptico virtual
	_ 03. Seletor de Discos Ópticos
	_ 		Acrescentar
	_ 		Selecione o arquivo de disco óptico virtual: ubuntu-20.04.3-live-server-amd64.iso
	_ 	<Abrir>
	_ 04. Not Attached
	_ 		Selecionar: ubuntu-20.04.3-live-server-amd64.iso
	_ 	<Escolher>
	_ <Iniciar>


Quarta etapa: Instalação e Configuração do Ubuntu Server 20.04.3 LTS<br>
Instalação do Ubuntu Server: https://ubuntu.com/server/docs/installation

	_ 01. Use UP, DOWN and ENTER keys to select your language 
	_ 		English - <Enter>
	_ 02. Keyboard configuration
	_ 		Layout: [English (US)]
	_ 		Variant: [English (US)]
	_ 	<Done>
	_ 03. Network connections
	_ 		enp0s3 eth <Enter>
	_ 			Edit IPv4 <Enter>
	_ 				IPv4 Method: Manual <Enter>
	_ 					Subnet: 172.16.1.0/24 <Tab>
	_ 					Address: 172.16.1.20 <Tab>
	_ 					Gateway: 172.16.1.254 <Tab>
	_ 					Name servers: 172.16.1.254 <Tab>
	_ 					Search domains: pti.intra
	_ 				<Save>
	_ 	<Done>
	_ 04. Configure proxy - <Done>
	_ 05. Configure Ubuntu archive mirror - <Done>
	_ 06. Guided storage configuration - <Done>
	_ 07. Storage configuration - <Done>
	_ 		Confirm destructive action - <Continue>
	_ 08. Profile setup
	_ 		Your name: Robson Vaamonde <Tab>
	_ 		Your server's name: ptispo01ws01 <Tab>
	_ 		Pick a username: vaamonde <Tab>
	_ 		Choose a passwords: pti@2018 <Tab>
	_ 		Confirm your passwords: pti@2018
	_ 	<Done>
	_ 09. SSH Setup
	_ 		Install OpenSSH server: ON <Space>
	_ 		Import SSH identity: No <Tab>
	_ 	<Done>
	_ 10. Featured Server Snaps - <Done>
	_ 11. Reboot Now - <Enter>
	_ 12. Please remove the installation medium, then press ENTER - <Enter>