INFOS ET PREREQUIS :

Ce projet en langage C implique des connaissances en réseau et spécifiquement en modèle OSI.
Il a été utilisé sous Linux uniquement.
Il est séparé en fichiers sources traitant des couches OSI différentes : transport, réseau, liaison de données, etc...
Il convient au préalable d'installer les bibliothèques pcap : 
sudo apt install libpcap-dev

---
UTILISATION :
---
Pour le lancer (en étant dans le bon dossier) :
make
sudo ./sniffer [-i <interface> -o <fichier> -f <filtre BPF>]

---
EXEMPLES :
---
sudo ./sniffer // mode par défaut
sudo ./sniffer -i lo // choisit l'interface loopback pour la capture
sudo ./sniffer -f "tcp and dst port 80" // filtre le trafic pour HTTP uniquement
sudo ./sniffer -o monfichier.pcap // utilise un fichier .pcap à la place


