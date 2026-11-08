<div align="center">
  <img alt="Cabeçalho do CantaPedrao" src="readme/header.png" style="border-radius: 15px; margin-bottom: 20px;" />

# CantaPedrao — Reprodutor de Karaokê

**Tenha uma experiência completa de karaokê asiático diretamente no seu computador, usando suas próprias músicas!**

![Versão](https://img.shields.io/badge/vers%C3%A3o-1.16.0-blue)
![Plataformas](https://img.shields.io/badge/plataformas-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
![Execução](https://img.shields.io/badge/execu%C3%A7%C3%A3o-offline-green)

</div>

<div align="center">
  <img alt="Demonstração do CantaPedrao" src="readme/demo.jpg" style="border-radius: 15px; margin-bottom: 20px; margin-top: 20px;" />
</div>

---

## Principais recursos

### Experiência de canto

#### Pontuação em tempo real

- O mecanismo de áudio **Forte**, baseado na Web Audio API, capta a voz pelo microfone.
- Acompanha a afinação em tempo real, detecta mudanças de tonalidade e exibe um guia visual de notas para ajudar você a alcançar as notas certas. Disponível em faixas Multiplex e MIDI compatíveis.
- Avalia não apenas a precisão da afinação, mas também a expressividade e a interpretação.

#### Controle de tom e latência

- Ajuste o tom (transposição) e o andamento da música durante a reprodução.
- Calibre rapidamente a latência do microfone e de toda a cadeia de áudio.

#### Romanização em japonês e coreano

- Cante músicas em japonês e coreano mesmo sem conhecer os sistemas de escrita: o programa gera a romanização das letras em tempo real.
- Também oferece suporte a Furigana (texto auxiliar de leitura) em arquivos MIDI de karaokê.

### Karaokê social e controle remoto

#### Encore Sessions — salas virtuais de karaokê

- Cante com amigos e familiares pela internet, mesmo à distância.
- Organize a fila de músicas, envie mensagens e interaja com os participantes.
- Divirta-se com placar e classificação de pontuações.
- Convide amigos pela integração com o Discord, sem precisar enviar um link manualmente.

#### EnMoku! — controle remoto pelo celular

- Leia o QR Code exibido na tela para conectar seu smartphone.
- Não é necessário instalar aplicativo: o EnMoku funciona diretamente no navegador. Compatível com navegadores baseados em Chromium (como Chrome e Edge) e Firefox.
- Adicione músicas à fila, envie mensagens, interaja com a sala e use a câmera do celular.
- Transforme o celular em um instrumento virtual de percussão (shaker).
- Funciona na rede local e pode utilizar um túnel na nuvem quando os dispositivos estiverem em redes diferentes.

#### Integração com Discord

- Exibe automaticamente no status do Discord a música que está sendo cantada.

### Reprodução e formatos de mídia

#### Suporte a diferentes formatos

- **Karaokê MIDI:** arquivos `.mid` e `.kar`, com SoundFonts `.sf2`, `.sf3` e `.dls`.
- **Áudio:** arquivos `.mp3`, `.wav`, `.m4a` e `.ogg`, acompanhados de letras `.lrc` ou arquivos CDG.
- **Vídeos musicais:** arquivos `.mp4`, `.mkv`, `.webm` e `.avi`.
- **Faixas Multiplex:** suporte ao controle dos canais esquerdo e direito para alternar entre voz guia e instrumental.

#### Integração nativa com YouTube

- Pesquise músicas diretamente pelo reprodutor ou pelo celular e adicione os resultados à fila de reprodução.

### Gravação, transmissão e ferramentas para criadores

#### Gravação instantânea

- Grave suas apresentações vocais diretamente no computador com apenas um comando.

#### Transmissão ao vivo por RTMP

- Transmita suas sessões de karaokê diretamente pelo programa.

#### Sobreposições para OBS

- Exiba a fila de músicas na transmissão, sem precisar alternar entre janelas para atualizá-la.
- Utilize uma sobreposição com as letras para que o público possa cantar junto.

#### Automação de cenas do OBS

- Alterne automaticamente as cenas do OBS durante a sessão de karaokê.

---

## Primeiros passos

### Configuração da biblioteca de músicas

> [!WARNING]
> Por restrições de direitos autorais, o CantaPedrao não inclui uma biblioteca de músicas. Você deve adicionar seus próprios arquivos, respeitando a legislação aplicável.

O programa procura automaticamente, nas unidades locais, uma pasta chamada **`EncoreLibrary`**. Você também pode importar uma pasta pelo **Gerenciador de Biblioteca**.

<div align="center">
  <img alt="Gerenciador de biblioteca" src="readme/library-manager.jpg" style="border-radius: 15px; margin-bottom: 20px; margin-top: 20px;" />
</div>

Para montar sua biblioteca, organize os arquivos seguindo este exemplo:

```text
D:/EncoreLibrary/                                      # Pasta da biblioteca (pode ter outro nome)
 ├── manifest.json                                     # Metadados e configurações de vídeos de fundo
 ├── [Artista] - [Música].mp3                          # Arquivo de áudio (compatível com etiquetas ID3)
 ├── [Artista] - [Música].lrc/.mid                     # Letra LRC correspondente ou guia MIDI
 ├── [Artista] - [Música].cdg                          # Arquivo CDG correspondente (opcional)
 ├── [Artista] - [Música].mp4                           # Vídeo musical
 ├── [Artista] - [Música].mid/.kar                     # Arquivo MIDI
 └── [Artista] - [Música].chorus.ogg                   # Vozes de apoio para MIDI (OGG recomendado)
```

**Observação:** em faixas Multiplex, nas quais a voz e o instrumental ficam em canais separados, inclua `.multiplexed.` no nome do arquivo antes da extensão. Exemplo: `Musica.multiplexed.mp3`.

---

## Controles e atalhos

O programa pode ser controlado pelo teclado ou pelo EnMoku.

| Tecla | Ação |
| :--- | :--- |
| `0–9` | Digitar o código da música para reservar ou reproduzir |
| `Enter` | Confirmar a reserva ou reproduzir a música selecionada |
| `Escape` | Parar a reprodução, limpar a entrada ou voltar |
| `Espaço` | Pausar ou continuar a reprodução |
| `L` | Abrir a personalização das letras |
| `Y` | Abrir a pesquisa de músicas locais e do YouTube |
| `Q` | Abrir a fila de reservas |
| `M` | Abrir o mixer e ajustar os volumes do microfone e da música |
| `R` | Iniciar/parar a gravação ou consultar gravações |
| `S` | Abrir o menu de sessões |
| `B` | Abrir o menu de transmissão |
| `T` | Abrir o bate-papo durante uma sessão |
| `C` | Ativar ou desativar as vozes de apoio |
| `-` / `=` | Diminuir ou aumentar o volume |
| `Shift + - / =` | Ajustar o volume de monitoração do microfone |
| `Seta para cima / baixo` | Alterar o tom durante a reprodução ou navegar pela lista |
| `Seta para esquerda / direita` | Alternar o canal de voz guia nas faixas Multiplex |
| `'` / `"` | Alterar os padrões de bateria |
| `[` / `]` | Alternar vídeos de fundo ou ajustar a sincronização do vídeo |
| `F2` | Entrar no modo de configurações (no menu principal) |

---

## Configurações do sistema

Pressione **`F2`** no menu principal para acessar o **Modo de Configuração**. O acesso é protegido por PIN (padrão: `0000`). Nesse menu, você pode:

- Alterar o caminho da biblioteca de músicas.
- Selecionar o microfone (entrada) e os alto-falantes (saída).
- Configurar o SoundFont e os dispositivos de saída MIDI.
- Ajustar o volume geral e a compensação de latência do microfone.
- Calibrar a sincronização do vídeo.
- Definir uma mensagem de boas-vindas em tela cheia para a tela de espera do seu estabelecimento.
- Alterar o PIN de segurança (recomendado).

---

## Instalação e execução para desenvolvimento

### Instaladores

Os instaladores e pacotes prontos para uso estão disponíveis na página de [Versões do CantaPedrao](https://github.com/DevKove/CantaPedrao/releases).

> [!NOTE]
> As versões de 1.0.0 a 1.3.1 são compatíveis com Windows. A partir da versão 1.4.0, há suporte a Linux. O suporte a macOS está disponível a partir da versão 1.10.0.

### Requisitos para compilar

- Node.js e npm.
- Git.
- Dependências do projeto instaladas.

### Compilar e executar

1. **Clonar o repositório:**

   ```bash
   git clone https://github.com/DevKove/CantaPedrao.git
   cd CantaPedrao
   ```

2. **Instalar as dependências:**

   ```bash
   npm install
   ```

3. **Executar em modo de desenvolvimento:**

   ```bash
   npm run start
   ```

4. **Gerar os pacotes para a plataforma atual:**

   ```bash
   npm run make
   ```

**Modo quiosque:** para iniciar em tela cheia e desativar o Windows Explorer quando aplicável, utilize o parâmetro `--kiosk`.

### Contribuição

Consulte o documento [CONTRIBUTING.md](CONTRIBUTING.md) para obter orientações sobre como contribuir com o projeto.

Para uma melhor experiência de desenvolvimento, recomendamos o [Visual Studio Code](https://code.visualstudio.com) com a extensão Prettier.

---

## Créditos e agradecimentos

### Bibliotecas e projetos utilizados

- **Estrutura principal:** [Cherry Tree / Terebi](https://github.com/terebiorg/terebi).
- **Reprodução de áudio:**
  - Metadados ID3: [jsmediatags](https://github.com/aadsm/jsmediatags).
  - Reprodução MIDI: [SpessaSynth](https://github.com/spessasus/SpessaSynth).
  - Detecção de afinação: [Pitchy](https://github.com/ianprime0509/pitchy).
  - Detecção de tonalidade: [Meyda](https://meyda.js.org/).
- **Romanização:**
  - Japonês: [Kuroshiro](https://kuroshiro.org/).
  - Coreano: [Aromanize](https://github.com/fujaru/aromanize-js/).
- **Integração com Discord:** [discord-rpc](https://github.com/xhayper/discord-rpc).

### Pessoas que contribuíram para o projeto original

- **[Stariix](https://www.youtube.com/@Stariixy):**
  - Desenvolvimento dos vídeos de fundo em 3D.
  - Vozes utilizadas nos efeitos sonoros de pontuação.
  - Criação e design dos mascotes Akiyama Hoshi e Kurayami Kai.
- **[MTSyntho](https://github.com/MTSyntho):** recursos para suporte ao Linux.
- **[prjoni99](https://github.com/prjoni99):**
  - Recursos para suporte ao macOS.
  - Identificação de possíveis falhas de segurança iniciais.
- **[Spessasus](https://github.com/spessasus/):**
  - Criador do SpessaSynth, sintetizador utilizado pelo programa.
  - Sugestões de código e contribuições técnicas para o SpessaSynth.
- **[Objecty](https://www.youtube.com/@objecty):** design dos indicadores de formato.
- **[Lap](https://github.com/ItsLap)** e **[Kat21](https://github.com/datkat21):** criadores do núcleo Cherry Tree, estrutura que serve de base ao programa.

---

## Idioma

Este README está em **português do Brasil (pt-BR)**. A tradução desta documentação não significa que toda a interface do programa já esteja traduzida.
