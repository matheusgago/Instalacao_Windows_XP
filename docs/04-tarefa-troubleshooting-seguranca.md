# Etapa 4: Troubleshooting e Redes no VirtualBox

## 🎯 Objetivo
Solucionar travamentos comuns do VirtualBox ao lidar com sistemas legados e mitigar riscos de segurança através do isolamento de placas de rede virtuais.

---

## 📑 Roteiro de Execução

1.  **Troubleshooting de Integração (Se necessário):**
    *   Se o mouse travar ou sumir após a instalação, vá nas configurações da VM no VirtualBox, aba **Sistema** -> **Dispositivo de Apontamento** e mude de `Multi-touch Tablet` para `Mouse PS/2`.
2.  **Configuração de Rede Segura (Isolamento de Vulnerabilidades):**
    *   O Windows XP é vulnerável a ataques modernos de rede distribuída (como o exploit *EternalBlue* / *WannaCry*).
    *   Abra as configurações da VM no VirtualBox com ela desligada. Vá na aba **Rede**.
    *   No campo **Conectado a:** altere a opção padrão `NAT` para **Não Conectado** ou **Rede Interna (Internal Network)**.
    *   Isso garante que o sistema compartilhe arquivos com outras VMs do laboratório (se necessário), mas fique totalmente blindado e invisível contra varreduras e ataques vindos da Internet real.

---

## 📝 Entregáveis desta Etapa

### 📸 [EVIDÊNCIA]
*<img width="802" height="478" alt="image" src="https://github.com/user-attachments/assets/7265cd51-fb3a-4938-8e17-aa0df34801f0" />
*

### ❓ [QUESTÃO 4]
Se mantivéssemos o adaptador de rede da máquina virtual do Windows XP configurado no modo "Placa em modo Bridge (Bridged Adapter)" conectada à rede Wi-Fi/cabeada pública da instituição, quais seriam as consequências imediatas em termos de segurança cibernética para o laboratório e para a VM?

**Sua Resposta:**
> Se a máquina virtual do Windows XP permanecesse configurada em modo Bridge conectada à rede pública da instituição, ela ficaria exposta diretamente aos demais dispositivos da rede. Como o Windows XP é um sistema operacional antigo e sem atualizações de segurança, a VM se tornaria vulnerável a ataques, malwares e invasões. Além disso, um comprometimento da máquina virtual poderia representar riscos para o laboratório e para a rede institucional, permitindo propagação de ameaças e acesso indevido a outros dispositivos. Por isso, em laboratórios virtuais, recomenda-se utilizar NAT ou redes isoladas para aumentar a segurança.

---
### 🏁 FIM DA ATIVIDADE
Com todas as seções preenchidas e imagens anexadas à pasta `/assets` do seu repositório local, execute os comandos do Git para registrar e subir sua atividade:

```bash
git add .
git commit -m "feat: conclusao do laboratorio de instalacao do winxp no virtualbox"
git push origin main
