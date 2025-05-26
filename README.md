
# MotoG04_Termux_UnlockBootloader

**Desbloqueie o Bootloader dos dispositivos Moto G04/G04S utilizando apenas outro celular Android com Termux e Cabo OTG, sem necessidade de computador.**

> [**Read this page in English**](https://github.com/gates-alt/MotoG04_Termux_UnlockBootloader/blob/main/README_en.md)

---

## **⚠️ Aviso de Isenção de Responsabilidade ⚠️**

> **ATENÇÃO:**  
> Eu, [@gatesgsm](https://t.me/gatesgsm), criador e mantenedor deste projeto, **não me responsabilizo** por quaisquer danos causados ao seu dispositivo ao utilizar os scripts ou métodos aqui disponibilizados.  
>  
> **Use por sua conta e risco.** É fundamental entender os procedimentos antes de executá-los.

---

## **Precisa de ajuda?**

Se você enfrentar problemas durante o processo ou precisar restaurar os bootloaders, estou disponível para ajudar via **Telegram**:  
**[@gatesgsm](https://t.me/gatesgsm)**

> Dica: O script `restore_boot.sh` geralmente resolve a maioria dos problemas de inicialização.

---

## Compatibilidade

Este projeto é **totalmente compatível com todos os modelos, variantes, regiões e tipos** do **Moto G04 e Moto G04S**.

> Sempre que menciono “Moto G04”, também estou me referindo ao **Moto G04S**, pois ambos utilizam a mesma base de hardware e software, sendo essencialmente o mesmo aparelho para os propósitos deste projeto.

---

## **Requisitos**

Você vai precisar de:

- Um **celular Android secundário** (host), onde o Termux será executado
- Aplicativos:
  - [**Termux**](https://f-droid.org/en/packages/com.termux/)
  - [**Termux:API**](https://f-droid.org/en/packages/com.termux.api/)
- Um **cabo OTG**
- Um **cabo de dados USB** (USB-A para USB-C)

---

## **Preparando o Testpoint**

Para desbloquear seu celular (ou simplesmente se conectar no **modo interativo FDL2**), será necessário realizar o **testpoint**, um procedimento que envolve abrir o dispositivo e tocar um ponto específico na placa-mãe.

### **Vídeos úteis:**

- [**Como remover a tampa traseira do Moto G04/G04S**](https://youtube.com/shorts/x3WhoOhb4js?feature=shared)  
- [**Como fazer o testpoint no Moto G04/G04S**](https://youtu.be/QMFQPKndK64?feature=shared)

---

## **Instalação e Uso**

### **1. Instale os aplicativos necessários**

Baixe o [**Termux**](https://f-droid.org/en/packages/com.termux/) e o [**Termux:API**](https://f-droid.org/en/packages/com.termux.api/) via **F-Droid** para garantir versões seguras e atualizadas.

### **2. Conceda permissões ao Termux:API**

Abra o **Termux:API** e conceda as permissões solicitadas para que o Termux possa interagir com o hardware.

### **3. Baixe e instale o projeto**

No Termux, execute:

```bash
curl -sL https://raw.githubusercontent.com/gates-alt/MotoG04_Termux_UnlockBootloader/main/install.sh | bash && cd MotoG04_Termux_UnlockBootloader
```

---

### **4. Prepare a conexão**

- Conecte o **cabo OTG** ao celular host (aquele que está com o Termux).
- Conecte a ponta **USB-A** do cabo de dados ao cabo OTG.
- **Não conecte a ponta USB-C** ao Moto G04/G04S ainda!

---

### **5. Execute o script desejado**

Você pode rodar um dos scripts disponíveis no projeto. Por exemplo, para desbloquear o bootloader:

```bash
./unlockbootloader.sh
```

---

### **6. Faça o testpoint e conecte o G04**

- Após iniciar o script no Termux, ele ficará aguardando a conexão do seu Moto G04.
- Faça o **testpoint** no dispositivo conforme demonstrado nos vídeos (ver seção anterior).
- **Enquanto mantém o testpoint**, conecte a ponta USB-C do cabo de dados ao Moto G04.
- Pode aparecer uma solicitação de permissão USB no celular host — **autorize**.
- Aguarde o processo ser concluído.

---

## **Recuperação com `restore_boot.sh`**

O script `restore_boot.sh` **não utiliza backups salvos automaticamente**.  
Ele carrega os **bootloaders confiáveis do firmware original**, localizados na pasta `uboot_spl/`.

Essa abordagem é proposital: evita restaurar arquivos corrompidos e aumenta a segurança do processo de recuperação.

---

## **Como usar o `restore_boot.sh`**

Este script é utilizado para **recuperar o Moto G04 brickado**, ou seja, quando ele **não liga e nem entra mais em modo fastboot**.

### **Passos para recuperação:**

1. Conecte o cabo OTG ao celular host e plugue o cabo de dados (USB-A).
2. **Deixe a ponta USB-C desconectada do Moto G04.**
3. Execute o script no Termux:

```bash
./restore_boot.sh
```

4. **Enquanto o script estiver aguardando:**
   - Conecte a ponta USB-C ao Moto G04.
   - **Segurar o botão Volume Menos pode ajudar**, mas não é obrigatório.

5. Autorize a permissão USB, se necessário, e aguarde a conclusão do processo.

---

## **Créditos**

Este projeto foi possível graças ao trabalho do desenvolvedor [**TomKing062**](https://github.com/TomKing062), criador das ferramentas utilizadas aqui.

- Os binários foram **compilados e organizados por mim, [@gatesgsm](https://t.me/gatesgsm)**.
- A autoria dos exploits e utilitários pertence a TomKing062.

### **Repositórios originais:**

- [TomKing062/spreadtrum_flash](https://github.com/TomKing062/spreadtrum_flash)  
- [TomKing062/CVE-2022-38694_unlock_bootloader](https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader)

---

## **Recomendações Finais**

- Use **cabos de boa qualidade** para evitar falhas na comunicação com o dispositivo.
- Nunca desconecte o aparelho ou feche o Termux enquanto scripts estiverem em execução.
- Em caso de falhas, sempre tente o script `restore_boot.sh` antes de realizar outros procedimentos.

---

## **Contato**

Caso precise de suporte ou queira colaborar com o projeto:

- Telegram: [@gatesgsm](https://t.me/gatesgsm)
- GitHub: [github.com/gates-alt/MotoG04_Termux_UnlockBootloader](https://github.com/gates-alt/MotoG04_Termux_UnlockBootloader)

---
