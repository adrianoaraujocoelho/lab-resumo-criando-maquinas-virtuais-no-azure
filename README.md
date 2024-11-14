# Criando Máquinas Virtuais no Azure
Este guia oferece instruções detalhadas para criar e configurar máquinas virtuais (VMs) no Microsoft Azure, permitindo que você aproveite os recursos de computação em nuvem com flexibilidade e escalabilidade.

Índice
Introdução
Pré-requisitos
Passo a Passo para Criar uma VM
Configurações Adicionais
Melhores Práticas
Documentação e Suporte
Introdução
O Microsoft Azure permite que você crie e gerencie máquinas virtuais para executar diferentes sistemas operacionais, como Windows e Linux. As VMs são úteis para desenvolvimento, teste, e até execução de cargas de trabalho em produção.

Pré-requisitos
Conta do Azure: Uma conta ativa no Microsoft Azure. Se ainda não tem, crie uma conta gratuita.
Permissões Adequadas: Acesso de administrador para criar e gerenciar recursos no Azure.
Familiaridade com Azure Portal ou CLI: O Azure Portal, CLI ou PowerShell podem ser usados para criar a VM.
Passo a Passo para Criar uma VM
Método 1: Criar uma VM pelo Portal do Azure
Acesse o Azure Portal.
No painel de navegação, selecione Máquinas Virtuais.
Clique em Criar e escolha Máquina Virtual.
Preencha os campos necessários:
Assinatura e Grupo de Recursos
Nome da VM e Região
Imagem do sistema operacional (ex.: Windows Server ou Ubuntu)
Tipo de Tamanho da VM (CPU e memória)
Em Configurações de Acesso e Segurança, configure:
Método de Autenticação (Senha ou chave SSH)
Regras de Porta (ex.: RDP para Windows ou SSH para Linux)
Revise as configurações e clique em Criar.
Método 2: Criar uma VM com a Azure CLI
bash
Copiar código
az vm create \
  --resource-group MeuGrupoDeRecursos \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username adminUsuario \
  --generate-ssh-keys
Este comando cria uma VM Linux com uma chave SSH gerada automaticamente e com imagem Ubuntu.

Configurações Adicionais
Discos: Adicione discos para mais armazenamento conforme necessário.
Rede: Configure redes virtuais, grupos de segurança e regras de firewall para controle de acesso.
Escalabilidade: Configure autoscaling ou conjuntos de disponibilidade para garantir alta disponibilidade.
Melhores Práticas
Escolha o Tamanho Adequado: Selecione uma VM que atenda aos requisitos de carga de trabalho considerando custo e desempenho.
Configure a Segurança: Utilize senhas fortes, autenticação baseada em chave SSH e controle de acesso via firewall.
Automatize Backup e Recuperação: Configure backups automáticos para proteção de dados.
Monitore a VM: Use o Azure Monitor para rastrear a performance e configurar alertas de incidentes.
Documentação e Suporte
Para mais detalhes, consulte a Documentação do Azure. Para ajuda adicional, utilize o Suporte Azure.

Este README foi elaborado para facilitar o processo de criação de VMs no Azure e ajudar a garantir que todas as configurações e práticas recomendadas estejam implementadas.
