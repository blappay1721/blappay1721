<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg">
  <img alt="Bernard Lappay. Computer Engineering, UC San Diego." src="./assets/banner-light.svg" width="100%">
</picture>

I build systems at every level, from logic gates to the servers they run on. I study Computer Engineering at UC San Diego (B.S. June 2027), run a containerized game network for 30+ players on a homelab I built, fine-tune and serve LLMs on my own hardware, and write plugins that run on live servers.

**Looking for IT infrastructure, ML, and DevOps roles starting June 2027.** My portfolio and résumé are at [blappay1721.github.io](https://blappay1721.github.io/). Reach me at [blappay1721@gmail.com](mailto:blappay1721@gmail.com) or on [LinkedIn](https://www.linkedin.com/in/blappay1721).

## Now

- **Technical contributor at Silent Studio.** Gameplay and backend work on [Mineshoku Tensei](https://mineshokutensei.com/), a live multiplayer game. I cut a core spatial-query system's geometry data by about 86%, closed an exploit across dozens of config files with a scripted, diff-verified rollout, and audited 2,295 default permissions.
- **Running my homelab.** One 16 GB mini PC hosts a Minecraft network, a Discord bot and a local LLM. Every game server runs in a container, the largest worlds start on demand, and no admin port is open to the internet.

## Selected work

### Infrastructure and servers

| Project | What it is | Result |
| :-- | :-- | :-- |
| [Self-hosted game server platform](https://blappay1721.github.io/#projects) | Docker and Pelican, admin access only through Cloudflare Tunnel with 2FA and Tailscale, fail2ban tuned on real logs, hourly restic backups to an append-only copy | Moved live into Docker in one day with no data lost |
| [UncapDefense](https://github.com/blappay1721/UncapDefense) | Paper plugin that lifts Minecraft's 80% armor damage-reduction cap with smooth, hot-reloadable curves | One jar, boot-tested on 11 server versions from 1.16.5 to 26.3 |
| [PlacedOnlyBreak](https://github.com/blappay1721/placedonlybreak) | Resettable build arenas: players break only blocks placed this round, and the plugin fails closed | Runs on 3 live servers; one Java 8 jar for 1.13.2 to 26.3 |
| [AwesomeChat DiscordSRV Addon](https://github.com/blappay1721/AwesomeChat-DiscordSRV-Addon) | Port of the InteractiveChat DiscordSRV addon to AwesomeChat: renders in-game items, inventories and ender chests into Discord | 25 Minecraft versions supported; 19 legacy modules and dependencies removed |

### Machine learning and LLMs

| Project | What it is | Result |
| :-- | :-- | :-- |
| [bruh, a Discord bot](https://github.com/blappay1721/bruh) | Persona chat from a fine-tuned 1.7B model (QLoRA, then DPO), plus private in-place translation with an encrypted cache | 36 personas served locally from one 4-bit model; the cache holds only ciphertext |
| [Math-reasoning inference pipeline](https://github.com/blappay1721/151B_SP26_Competition) | Makes a fixed 4B model more reliable at math: sampling, voting, a verifier and retries, run with vLLM on rented H100s | 68/100, ranked #29 of 105, solo against teams of up to 4 |
| [Movie recommender with EM](https://github.com/blappay1721/EM-Movie-Recommender) | Expectation-Maximization written from scratch in NumPy, learning audience types from a survey with 40% of ratings missing | Final log-likelihood matches the course reference to four decimal places |
| [Handwritten digit recognition](https://github.com/blappay1721/MNIST-NN-Classifier) | Vectorized NumPy nearest-neighbor classifier with a [draw-a-digit demo](https://blappay1721.github.io/MNIST-NN-Classifier/) | 95.4% accuracy; the whole test set classified in about 0.25 s |

### Digital design

| Project | What it is | Result |
| :-- | :-- | :-- |
| [Microprogrammed signed multiplier](https://github.com/blappay1721/robertsons-multiplier-sv) | Robertson's algorithm in SystemVerilog: a datapath run by a microcode-ROM control unit | All 16,384 pairs of 7-bit signed operands pass an exhaustive testbench |
| [LFSR message encryptor](https://github.com/blappay1721/lfsr-encryptor-sv) | Hardware stream cipher: a 6-bit LFSR keystream encrypts a message held in on-chip memory | 64 of 64 output bytes match a software model |
| [Alarm clock with calendar](https://github.com/blappay1721/alarm-clock-sv) | Three versions, up to day-of-week and calendar, built from one reusable modulo-N counter | Testbenches print the seven-segment displays as ASCII |

## Toolbox

**Infrastructure:** Ubuntu Server, Docker, systemd, Pelican, restic, LVM, MariaDB, Grafana\
**Networking and security:** Tailscale, Cloudflare Tunnel, ufw, iptables, fail2ban, tcpdump, Pi-hole\
**Machine learning:** PyTorch, vLLM, Hugging Face (TRL, PEFT), QLoRA, DPO, llama.cpp, Ollama\
**Languages:** Java, Python, JavaScript, C, C++, SystemVerilog, Bash
