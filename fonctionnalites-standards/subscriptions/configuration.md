# Configuration

## 1\) Activez les commandes récurrentes <a id="1-enable-subscriptions"></a>

_Pendant la durée du mode béta, contactez-nous si vous souhaitez utiliser le module pour que nous puissions l'activer sur votre profil._

Activez le module en vous rendant sur les paramètres de votre profil :

![](../../.gitbook/assets/image%20%2882%29.png)

**Abonnements :** Pour activer, sélectionnez "Activée".

**Commandes des invités** : Nous vous recommandons de désactiver cette option afin de ne pas risquer des doublons de commandes.

**Modifier la commande** : 

* Si vous permettez à l'acheteur de modifier la commande il va pouvoir à chaque nouvelle commande automatique modifier les quantités achetées et retirer des produits. Pour en ajouter, il devra faire une nouvelle commande.
* Dans le cas contraire, ils devront vous contacter pour réaliser des modifications. Ils pourront cependant toujours réaliser une nouvelle commande.

## 2\) Vérifiez les méthodes de paiement et de livraison <a id="2-make-sure-you-have-shipping-and-payment-methods-setup"></a>

Lorsque vous créez une commande récurrente pour un acheteur, il faut que vous indiquiez la méthode de paiement et de livraison choisie.

#### **Méthodes de livraison** <a id="shipping-methods"></a>

Il n'y a pas de restriction sur les méthodes de livraison utilisées. Pour la configuration des méthodes de livraison consultez[ la page suivante](../mise-en-place-dune-boutique/types-de-livraisons.md). 

#### **Méthode de paiement** <a id="payment-methods"></a>

**Vous ne pouvez utiliser que deux méthodes de paiement pour les commandes récurrentes**. Consultez [cette page](configuration.md#payment-methods) pour la configuration des méthodes de paiement.

**1\) Méthode manuelle** : Espèce ou virement.

**2\) Stripe :** Stripe est un outil de paiement par carte bancaire équivalent à Paypal \(l'obligation de créer un compte pour l'acheteur en moins\). A chaque commande, la carte bancaire va être débitée du montant de la commande \(modifications incluses\), sauf si la commande récurrents a été mise en pause ou annulée.

{% hint style="info" %}
Pour que l'acheteur soit correctement débité, il est nécessaire qu'il dispose d'un compte sur la plateforme Open Food France, qu'il ait enregistré une carte de crédit par défaut et donné l'autorisation à votre boutique de réaliser des prélèvements automatiques. Pour plus d'informations consultez la page [Pour l'acheteur](pour-lacheteur.md).
{% endhint %}

Également, si vous utilisez Stripe, pensez à bien nommer cette méthode de paiement dans votre interface d'administration.

Par exemple, au lieu de l'appeler "Paiement par carte bancaire", vous pouvez l'appeler "paiement automatique pour commande récurrente". Une description possible à ajouter : "Votre carte de crédit par défaut sera utilisée pour chaque commande récurrente non mise en pause ou annulée".

## 3\) Récupérer les informations auprès de vos acheteurs <a id="3-gather-information-from-your-customers"></a>

Pour créer un abonnement pour vos acheteurs, vous allez avoir besoin de certaines informations :

**Nom**, **numéro de téléphone** et **adresse e-mail.** Comme précisé dans le paragraphe suivant, tout acheteur souhaitant bénéficier de commandes récurrentes a l'obligation de se créer un compte sur OFF. Pour créer leur compte, vous aurez besoin de ces informations.

**Adresse de facturation et de livraison**

**Produits :** pour quels produits souhaitent-ils bénéficier d'une commande récurrente ?

**Méthode de livraison** 

**Méthode de paiement** 

**Dates** : la date de début et de fin de la commande récurrente. Pour rappel, les dates de début peuvent être situées avant ou après la date de début du cycle de vente, en revanche les dates de fin doivent obligatoirement se situer après la date de fin du cycle de vente.

## 4\) Ajoutez les nouveaux acheteurs à votre liste <a id="4-add-your-subscribers-to-your-customer-list"></a>

Avant de démarrer une commande récurrente pour un utilisateur, vous devez l'ajouter à votre liste d'acheteurs. 

**Une fois ajouté à votre liste,** demandez-leur de se créer un compte sur OFF. Toutes les étapes à réaliser de leur côté sont disponibles à la page [Pour l'acheteur](pour-lacheteur.md).

Vous pouvez aussi les ajouter à votre liste une fois leur compte créé. Dans tous les cas, il est nécessaire pour l'acheteur de disposer d'un compte sur la plateforme est de valider son adresse email. Par ailleurs, si vous utilisez Stripe en tant que méthode de paiement, il est nécessaire de les ajouter à votre liste d'acheteurs **AVANT qu'ils autorisent votre boutique à réaliser des prélèvements**.

## 5\) Les rythmes d'abonnement <a id="5-schedules"></a>

S'il s'agit de votre première utilisation d'OFF, nous vous conseillons de vous familiariser tout d'abord avec le concept de [cycle de vente](../mise-en-place-dune-boutique/cycle-de-vente-pour-les-hub.md).

### A propos <a id="about-schedules"></a>

Le module de commande récurrente fonctionne de manière à ce qu'a chaque réouverture de cycle de vente, les commandes sont générées automatiquement pour les acheteurs ayant une commande récurrente avec la boutique en question. Cependant il est important de noter que le système est suffisamment flexible pour autoriser les boutiques à décider _quel_ cycle de vente autorise des commandes récurrentes. Ainsi si vous disposez de plusieurs [cycles de ventes simultanés](../mise-en-place-dune-boutique/opening-more-than-one-order-cycle.md), tous ne sont pas obligés d'accepter les commandes récurrentes.

Au delà de la simple activation / désactivation de la fonctionnalité par cycle de vente, les commandes récurrentes sont associées à des rythmes d'abonnement \(hebdomadaire, mensuel, bi-mensuel,...\). Lorsqu'un rythme d'abonnement a été créé et associé à des commandes récurrentes, ces commandes ne seront lancées que pour les nouveaux cycles de vente reliés à ce rythme d'abonnement.

### Créer un rythme d'abonnement <a id="create-a-schedule"></a>

Une fois les premières étapes réalisées, vous allez voir apparaître le bouton "rythme d'abonnement" dans le menu Cycle de vente. Cliquez dessus pour créer un nouveau rythme d'abonnement :

![](../../.gitbook/assets/image%20%2820%29.png)

{% hint style="info" %}
Attention, vous devez au moins avoir un cycle de vente ouvert pour pouvoir configurer un rythme d'abonnement.
{% endhint %}

![](../../.gitbook/assets/image%20%2852%29.png)

**Nom :** Pensez à donner un nom logique au rythme d'abonnement. Par exemple : "hebdomadaire", "mensuel", "un jeudi sur deux"... Ce nom n'est pas visible pour les acheteurs.

Vous pouvez déplacer les cycles de ventes en utilisant les &lt; et &gt; boutons.

Cliquez sur "Créer" lorsque vous avez terminé.

### Modifier ou supprimer un rythme d'abonnement <a id="edit-or-delete-a-schedule"></a>

Pour modifier ou supprimer un rythme, cliquez sur son nom dans la colonne correspondante. Cette colonne doit peut-être être rendue visible grâce à ce menu sur la page Cycle de vente :

![](../../.gitbook/assets/image%20%2899%29.png)

{% hint style="info" %}
Vous ne pouvez pas supprimer un rythme d'abonnement si des commandes récurrentes y sont associés.
{% endhint %}

### Ajouter ou supprimer un cycle de vente d'un rythme d'abonnement <a id="adding-or-removing-order-cycles-from-schedules"></a>

Soit vous utilisez la fonctionnalité de modification d'un rythme décrite ci-dessus, soit vous pouvez utiliser la fonction présente dans la modification d'un cycle de vente :

![](../../.gitbook/assets/image%20%2823%29.png)

N.B. : Un même cycle de vente peut se retrouver dans plusieurs rythmes d'abonnement !

