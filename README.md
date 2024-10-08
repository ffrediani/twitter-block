Este script é utilizado para auxiliar nos bloqueios solicitados para o X / Twitter. Foi desenvolvido para ser compatível com sistemas operacionais Linux e macOS.

## Disclaimer

Existem controvérsias sobre a extensão da aplicação desses bloqueios e algumas pessoas entendem que a aplicação de blackhole ou filtros BGP dos prefixos do ASN através de rotas estáticas ou prefix list vai além do que foi solicitado para bloqueio da aplicação/conteúdo.

O usuário deve avaliar cuidadosamente com seus próprios meios os métodos de bloqueio pertinentes e que considere suficientes para atender ao que foi solicitado, levando em consideração o impacto sobre outros serviços e a eficácia do bloqueio.

A responsabilidade pelo uso deste script e suas consequências é inteiramente do administrador da rede e/ou do responsável pela operação.

## Funções

- **Rotas Estaticas IPv4 referente aos ASNs do X;**
- **Rotas Estaticas IPv6 referente aos ASNs do X;**
- **Entradas em DNS Recursivo (Unbound e Bind9);**
- **Prefix List baseada nos ASNs do X. Função para diversos [**vendors**](https://github.com/andrediashexa/twitter-block?tab=readme-ov-file#lista-de-vendors-suportados-para-prefix-list-mesmos-que-o-bgpq4-suporta).**


## Pré-requisitos

Para que o script funcione corretamente, é necessário ter as seguintes dependências instaladas:

- **BGPQ4**
- **IPCALC**
- **SIPCALC** (Devido ao IPv6)

## Lista de fabricantes e sistemas operacionais suportados para blackhole:

1. Cisco;
2. Juniper;
3. Nokia;
4. Huawei;
5. Mikrotik;
6. VyOS;
7. Linux;
8. FreeBSD.

## Lista de vendors suportados para prefix-list (Mesmos que o BGPQ4 suporta):

1. Huawei;
2. Huawei (XPL);
3. Cisco IOS-XE;
4. Cisco IOS-XR;
5. Juniper (Route-Filter);
6. Mikrotik v6;
7. Mikrotik v7;
8. Nokia MD-CLI;
9. Nokia SR-LINUX;
10. Nokia SROS Classic;
11. OpenBGPD;
12. BIRD;
13. Arista;
14. JSON Format.


**Observação:** O script foi testado nos fabricantes Cisco, Juniper e Huawei. Os demais fabricantes e sistemas operacionais listados ainda não foram testados.

## Instruções de Instalação

1. **Instale as dependências necessárias:**

   Para Linux:
   ```bash
   sudo apt update && sudo apt install git bgpq4 ipcalc sipcalc -y
   ```

   Para macOS:
   ```bash
   brew update && brew install git bgpq4 ipcalc
   ```

2. **Clone o repositório do GitHub:**

   ```bash
   git clone https://github.com/andrediashexa/twitter-block.git
   ```

3. **Acesse o diretório do projeto:**

   ```bash
   cd twitter-block
   ```

4. **Conceda permissão de execução ao script:**

   ```bash
   chmod +x run.sh
   ```

5. **Execute o script:**

   ```bash
   ./run.sh
   ```

6. **Selecione o fabricante ou sistema operacional desejado da lista apresentada e siga as instruções para concluir o processo.**
