---



copyright:
  years: 2017, 2018
lastupdated: "2010-03-19"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 2. Configuration de votre infrastructure
{: #set_up_infrastructure}

Vous trouverez dans la présente section tous les conseils nécessaires à la configuration de vos serveurs IBM Bare Metal SAP NetWeaver, que ce soit en matière de réseau, connectivité, sécurité, stockage ou système d'exploitation. Prenez contact avec le [support {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/docs/get-support/howtogetsupport.html#getting-customer-support) pour toute question.

## Commande de votre serveur
{: order-server}

Suivez les étapes ci-dessous pour commander vos serveurs Bare Metal. Vous trouverez des informations supplémentaires dans [Configuring your bare metal server](https://console.bluemix.net/docs/bare-metal/configuring.html#configuring-your-bare-metal-server).

1. Connectez-vous au [portail client de l'infrastructure {{site.data.keyword.cloud_notm}}](https://control.softlayer.com) à l'aide de vos identifiants uniques.
2. Cliquez sur l'icône **Devices** dans la page Account Summary.
3. Cliquez sur le lien **Monthly** sous les serveurs Bare Metal dans la page Devices. La boîte de dialogue présentant la liste des serveurs s'ouvre.
4. Les serveurs certifiés SAP figurent en début de liste. Cliquez sur l'hyperlien sous le **prix de départ au mois** pour sélectionner le serveur de votre choix et le déplacer vers la page de configuration/commande. 

   Les serveurs certifiés SAP NetWeaver sont facilement identifiables par la mention **-NW** sous Modèle CPU. La configuration du serveur Red Hat est décrite à l'étape 7 ci-après et à l'étape 1 de la section suivante Sélectionner les options de votre serveur. La procédure est identique sous Microsoft Windows. Notez que pour VMWare, le choix est plus limité, mais la procédure reste la même.
   
5. Entrez le nombre de serveurs que vous commandez dans la zone **Quality** et sélectionnez votre centre de données dans **Data Center**.
6. Les options relatives au **serveur**, à la **mémoire vive** et au stockage privé prennent la valeur par défaut du serveur sélectionné et ne sont pas modifiables. Vous commandez votre stockage {{site.data.keyword.IBM_notm}} {{site.data.keyword.blockstorageshort}} for {{site.data.keyword.cloud_notm}} ou {{site.data.keyword.filestorage_full_notm}} et Network Attached Storage (NAS) après avoir commandé votre serveur.
7. Sélectionnez votre système d'exploitation dans **Operating System** (Red Hat ou Microsoft), puis sélectionnez le système d'exploitation spécifique ou l'hyperviseur VMware pour votre serveur.

## Sélection de vos options de serveur
{: #select_options}

Au cours de l'étape suivante, vous allez sélectionner le type et le nombre de disques à ajouter à votre configuration. Vous pouvez aussi sélectionner des options différentes pour les groupes de stockage RAID (Redundant Array of Independent Disks) et les agencements de partition sur les groupes de stockage RAID. Pour plus d'informations, voir [About RAID](https://console.bluemix.net/docs/bare-metal/what-raid.html#about-raid) ou contactez le [support {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/docs/get-support/howtogetsupport.html#getting-customer-support).

1. Sous **Serveurs certifiés SAP**, effectuez votre sélection en fonction de la façon dont vous prévoyez d'utiliser votre serveur. Vous trouverez des détails sur chaque option dans la rubrique relative à la [configuration de vos serveurs Bare Metal](https://console.bluemix.net/docs/bare-metal/configuring.html#setting-up-your-bare-metal-servers). Vous pouvez aussi consulter la page de l'[outil de décision de conception](https://github.com/ibm-cloud-architecture/infrastructure-design-decision-tool) (faites défiler la page jusqu'à l'outil) ou prendre contact avec le [support {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/docs/get-support/howtogetsupport.html#getting-customer-support) pour plus d'informations.
2. Cliquez sur le bouton **Ajouter à la commande** situé au bas de la page.

## Définition de configurations système avancées
{: #adv_config}

1. Suivez les instructions présentées dans la rubrique [Advanced System Configuration](https://console.bluemix.net/docs/bare-metal/configuring.html#advanced-system-configuration) pour de l'aide relative aux valeurs figurant dans la fenêtre **Configuration système avancée**.

Les noms d'hôte SAP doivent être composés de 13 caractères alphanumériques maximum. Pour de plus amples renseignements sur les noms d'hôte SAP, voir les [notes SAP 611361](https://launchpad.support.sap.com/#/611361) et [129997](https://launchpad.support.sap.com/#/129997). 

Si vous avez décidé de configurer votre environnement en mode public/privé et que vous envisagez
  * D'installer plusieurs systèmes SAP ayant besoin de communiquer entre eux *ou*
  * De choisir une configuration SAP à trois niveaux (la base de données et les instances d'application étant installées sur du matériel différent)
  
Assurez-vous que la résolution de nom reflète les adresses interne et externe. L'adresse externe correspond au nom d'hôte du serveur qui a été résolu par son nom de domaine complet (FQDN). 

Les adresses internes n'apparaissent pas dans le système de résolution de nom (DNS). Sachant que les adresses IP internes peuvent être utilisées pour les communications entre les serveurs, assurez-vous d'étendre votre fichier `/etc/hosts` ou fichier "hôte" Microsoft Windows en conséquence. Ces informations s'appliquent également au système d'exploitation invité de vos déploiements VMware ESXi.

## Confirmation de vos sélections
{: #confirm_selections}

1. Validez vos choix sur la page de paiement et cochez les cases **Conditions des services Cloud** et **Contrat de licence logiciel tiers**.
2. Faites défiler la page vers le bas jusqu'à la partie Créer un compte. Entrez les informations de facturation et renseignez les zones **Type de paiement, Nom, Carte** et **Expiration** (date) relatives à la carte de paiement à utiliser pour la facturation.
3. Cliquez sur le bouton **Soumettre commande**. Vous êtes redirigé vers un écran affichant votre numéro de commande. Vous pouvez imprimer cette page, qui vous servira également d'accusé de réception de commande.

Un courrier électronique intitulé _{{site.data.keyword.cloud_notm}} Confirmation de la commande ##_ est alors envoyé à l'adresse que vous avez renseignée dans votre profil. Il indique que votre serveur a été approuvé et qu'il est sur le point d'être déployé. Une fois le serveur déployé, un autre avis indiquant que le serveur est disponible et qu'il peut être géré via le portail [{{site.data.keyword.cloud_notm}} Infrastructure Customer Portal](https://control.softlayer.com) vous est envoyé.

## Etapes suivantes

Vous pouvez maintenant commencer à gérer vos serveurs Bare Metal. Pour connaître la procédure correspondante, voir [Gestion de votre environnement SAP NetWeaver](/docs/infrastructure/sap-netweaver/sap-manage-environment.html).