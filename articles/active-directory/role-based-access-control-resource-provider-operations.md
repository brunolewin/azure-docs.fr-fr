---
title: Opérations du fournisseur Azure Resource Manager | Microsoft Docs
description: Décrit en détails les opérations disponibles sur les fournisseurs de ressources Microsoft Azure Resource Manager
services: active-directory
documentationcenter: ''
author: rolyon
manager: mtillman
ms.service: active-directory
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 03/06/2018
ms.author: rolyon
ms.openlocfilehash: 0b8c8823c6d21df96dcfd926db1855169f1570e4
ms.sourcegitcommit: 48ab1b6526ce290316b9da4d18de00c77526a541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2018
---
# <a name="azure-resource-manager-resource-provider-operations"></a>Opérations du fournisseur de ressources Azure Resource Manager

Ce document répertorie les opérations disponibles pour chaque fournisseur de ressources Microsoft Azure Resource Manager. Celles-ci peuvent être utilisées dans des rôles personnalisés pour fournir des autorisations de contrôle d’accès en fonction du rôle (RBAC) granulaires aux ressources dans Azure. Notez que cette liste n’est pas exhaustive et que des opérations peuvent être ajoutées ou supprimées à mesure que chaque fournisseur est mis à jour. Les chaînes d’opération sont au format `Microsoft.<ProviderName>/<ChildResourceType>/<action>`. 

> [!NOTE]
> Pour obtenir une liste complète et actuelle, utilisez `Get-AzureRmProviderOperation` (dans PowerShell) ou `az provider operation list` (dans Azure CLI v2) pour répertorier les opérations des fournisseurs de ressources Azure.

## <a name="microsoftaad"></a>Microsoft.AAD

| Opération | Description |
|---|---|
|/domainServices/delete|Supprime les services de domaine|
|/domainServices/read|Lit les services de domaine|
|/domainServices/write|Écrit les services de domaine|
|/locations/operationresults/read|Lit l’état d’une opération asynchrone|
|/Operations/read|Description conviviale localisée pour l’opération, telle qu’elle doit s’afficher à l’utilisateur.|

## <a name="microsoftaadiam"></a>microsoft.aadiam

| Opération | Description |
|---|---|
|/diagnosticsettings/delete|Désactive un paramètre de diagnostic|
|/diagnosticsettings/read|Lit un paramètre de diagnostic|
|/diagnosticsettings/write|Écrit un paramètre de diagnostic|
|/diagnosticsettingscategories/read|Lit les catégories d’un paramètre de diagnostic|
|/tenants/providers/Microsoft.Insights/diagnosticSettings/read|Obtient le paramètre de diagnostic pour la ressource|
|/tenants/providers/Microsoft.Insights/diagnosticSettings/write|Crée ou met à jour le paramètre de diagnostic pour la ressource|
|/tenants/providers/Microsoft.Insights/logDefinitions/read|Obtient les journaux disponibles pour les clients|

## <a name="microsoftadhybridhealthservice"></a>Microsoft.ADHybridHealthService

| Opération | Description |
|---|---|
|/configuration/action|Met à jour la configuration du client.|
|/configuration/read|Lit la configuration du client.|
|/configuration/write|Crée une configuration de client.|
|/services/action|Met à jour une instance de service dans le client.|
|/services/alerts/read|Lit les alertes pour un service.|
|/services/alerts/read|Lit les alertes pour un service.|
|/services/delete|Supprime une instance de service dans le client.|
|/services/read|Lit les instances de service dans le client.|
|/services/servicemembers/action|Crée une instance de membre de service dans le service.|
|/services/servicemembers/alerts/read|Lit les alertes pour un membre de service.|
|/services/servicemembers/delete|Supprime une instance de membre de service dans le service.|
|/services/servicemembers/read|Lit l’instance de membre de service dans le service.|
|/services/write|Crée une instance de service dans le client.|

## <a name="microsoftadvisor"></a>Microsoft.Advisor

| Opération | Description |
|---|---|
|/configurations/read|Obtenir des configurations|
|/configurations/write|Crée/met à jour la configuration|
|/generateRecommendations/action|Génère des recommandations|
|/generateRecommendations/read|Obtient l’état de génération de recommandations|
|/operations/read|Obtient les opérations pour le Microsoft Advisor|
|/recommendations/read|Lit les recommandations|
|/recommendations/suppressions/delete|Supprime la suppression|
|/recommendations/suppressions/read|Obtient les suppressions|
|/recommendations/suppressions/write|Crée/met à jour des suppressions|
|/register/action|Inscrit l’abonnement pour Microsoft Advisor|
|/suppressions/delete|Supprime la suppression|
|/suppressions/read|Obtient les suppressions|
|/suppressions/write|Crée/met à jour des suppressions|
|/unregister/action|Désinscrit l’abonnement pour le Microsoft Advisor|

## <a name="microsoftalertsmanagement"></a>Microsoft.AlertsManagement

| Opération | Description |
|---|---|
|/alerts/read|Obtient toutes les alertes pour les filtres d’entrée|
|/alerts/resolve/action|Modifie l’état de l’alerte en Résoudre|
|/alertsSummary/read|Obtient le résumé des alertes|
|/Operations/read|Lit les opérations fournies|

## <a name="microsoftanalysisservices"></a>Microsoft.AnalysisServices

| Opération | Description |
|---|---|
|/locations/checkNameAvailability/action|Vérifie que le nom d’Analysis Server donné est valide et non utilisé.|
|/locations/operationresults/read|Récupère les informations du résultat de l’opération spécifiée|
|/locations/operationstatuses/read|Récupère les informations de l’état de l’opération spécifiée|
|/operations/read|Récupère les informations d’opérations|
|/register/action|Inscrit le fournisseur de ressources Analysis Services|
|/servers/delete|Supprime l’Analysis Server.|
|/servers/listGatewayStatus/action|Affiche l’état de la passerelle associée au serveur|
|/servers/providers/Microsoft.Insights/diagnosticSettings/read|Obtient le paramètre de diagnostic pour Analysis Server|
|/servers/providers/Microsoft.Insights/diagnosticSettings/write|Crée ou met à jour le paramètre de diagnostic pour Analysis Server|
|/servers/providers/Microsoft.Insights/logDefinitions/read|Obtient les journaux disponibles pour la ressource|
|/servers/providers/Microsoft.Insights/metricDefinitions/read|Obtient les métriques disponibles pour Analysis Server|
|/servers/read|Récupère les informations de l’Analysis Server spécifié.|
|/servers/resume/action|Reprend l’Analysis Server.|
|/servers/skus/read|Récupère les informations de référence (SKU) disponibles pour le serveur|
|/servers/suspend/action|Suspend l’Analysis Server.|
|/servers/write|Crée ou met à jour l’Analysis Server spécifié.|
|/skus/read|Récupère les informations de références (SKU)|

## <a name="microsoftapimanagement"></a>Microsoft.ApiManagement

| Opération | Description |
|---|---|
|/checkNameAvailability/read|Vérifie si le nom du service indiqué est disponible|
|/operations/read|Lit toutes les opérations API disponibles pour la ressource Microsoft.ApiManagement|
|/register/action|Inscrire l’abonnement pour le fournisseur de ressources Microsoft.ApiManagement|
|/reports/read|Obtient des rapports agrégés par période de temps, région géographique, développeur, produit, API, opération, abonnement et demande.|
|/service/apis/delete|Supprimer l’API existante|
|/service/apis/diagnostics/delete|Supprime le diagnostic existant|
|/service/apis/diagnostics/loggers/delete|Supprime le mappage d’un enregistreur d’événements avec un paramètre de diagnostic|
|/service/apis/diagnostics/loggers/read|Obtient la liste des enregistreurs d’événements de diagnostic existants|
|/service/apis/diagnostics/loggers/write|Mappe un enregistreur d’événements à un paramètre de diagnostic|
|/service/apis/diagnostics/read|Obtient la liste des diagnostics ou obtient les détails d’un diagnostic|
|/service/apis/diagnostics/write|Ajoute nouveau diagnostic ou met à jour les détails du diagnostic existant|
|/service/apis/operations/delete|Supprimer l’opération d’API existante|
|/service/apis/operations/policies/delete|Supprime la configuration de stratégie des stratégies d’opération API|
|/service/apis/operations/policies/read|Obtient les stratégies pour l’opération API ou les détails de configuration de stratégie pour l’opération API|
|/service/apis/operations/policies/write|Définit les détails de configuration de l’opération API|
|/service/apis/operations/policy/delete|Supprimer la configuration de la stratégie de l’opération|
|/service/apis/operations/policy/read|Obtenir les détails de configuration de la stratégie pour l’opération|
|/service/apis/operations/policy/write|Définir les détails de configuration de la stratégie pour l’opération|
|/service/apis/operations/read|Obtenir la liste des opérations d’API existantes ou obtenir les détails de l’opération d’API|
|/service/apis/operations/tags/delete|Supprime l’association d’une balise existante avec une opération existante|
|/service/apis/operations/tags/read|Obtient les balises associées à l’opération ou les détails d’une balise|
|/service/apis/operations/tags/write|Associe une balise existante à une opération existante|
|/service/apis/operations/write|Créer une nouvelle opération d’API ou mettre à jour une opération d’API existante|
|/service/apis/operationsByTags/read|Obtient la liste des associations opération/balise|
|/service/apis/policies/delete|Supprime la configuration de stratégie des stratégies d’API|
|/service/apis/policies/read|Obtient les stratégies ou les détails de configuration de stratégie pour l’API|
|/service/apis/policies/write|Définir les détails de configuration de la stratégie pour l’API|
|/service/apis/policy/delete|Supprimer la configuration de la stratégie de l’API|
|/service/apis/policy/read|Obtenir les détails de configuration de la stratégie pour l’API|
|/service/apis/policy/write|Définir les détails de configuration de la stratégie pour l’API|
|/service/apis/products/read|Obtient tous les produits dont l’API fait partie|
|/service/apis/read|Obtenir la liste de toutes les API inscrites ou obtenir les détails de l’API|
|/service/apis/releases/delete|Supprime toutes les mises en production de l’API ou une mise en production de l’API|
|/service/apis/releases/read|Obtient les mises en production pour une API ou les détails d’une mise en production de l’API|
|/service/apis/releases/write|Crée une mise en production de l’API ou met à jour une mise en production existante de l’API|
|/service/apis/revisions/delete|Supprime toutes les révisions d’une API|
|/service/apis/revisions/read|Obtient les révisions appartenant à une API|
|/service/apis/schemas/delete|Supprime un schéma existant|
|/service/apis/schemas/document/read|Obtient le document décrivant le schéma|
|/service/apis/schemas/document/write|Met à jour le document décrivant le schéma|
|/service/apis/schemas/read|Obtient tous les schémas pour une API donnée ou les schémas utilisés par l’API|
|/service/apis/schemas/write|Définit les schémas utilisés par l’API|
|/service/apis/tagDescriptions/delete|Supprime la description de balise de l’API|
|/service/apis/tagDescriptions/read|Obtient les descriptions de balises ou une description de balise dans l’étendue d’une API|
|/service/apis/tagDescriptions/write|Crée/modifie une description de balise dans l’étendue de l’API|
|/service/apis/tags/delete|Supprime une association API/balise existante|
|/service/apis/tags/read|Obtient toutes les associations API/balise pour l’API ou les détails d’une association API/balise|
|/service/apis/tags/write|Ajoute une nouvelle association API/balise|
|/service/apis/write|Créer une nouvelle API ou mettre à jour les détails de l’API existante|
|/service/apisByTags/read|Obtient la liste des associations API/balise|
|/service/api-version-sets/delete|Supprime un VersionSet existant|
|/service/api-version-sets/read|Obtient la liste des entités d’un groupe de version ou les détails d’un VersionSet|
|/service/api-version-sets/versions/read|Obtient la liste des entités de version|
|/service/api-version-sets/write|Crée un VersionSet ou met à jour les détails d’un VersionSet existant|
|/service/applynetworkconfigurationupdates/action|Met à jour les ressources Microsoft.ApiManagement exécutées dans le réseau virtuel pour sélectionner les paramètres réseau mis à jour.|
|/service/authorizationServers/delete|Supprimer le serveur d’autorisation existant|
|/service/authorizationServers/read|Obtenir la liste des serveurs d’autorisation ou obtenir les détails du serveur d’autorisation|
|/service/authorizationServers/write|Créer un nouveau serveur d’autorisation ou mettre à jour les détails d’un serveur d’autorisation existant|
|/service/backends/delete|Supprimer le serveur principal existant|
|/service/backends/read|Obtenir la liste des serveurs principaux ou obtenir les détails du serveur principal|
|/service/backends/reconnect/action|Crée une demande de reconnexion|
|/service/backends/write|Ajouter un nouveau serveur principal ou mettre à jour les détails du serveur principal existant|
|/service/backup/action|Sauvegarder le service Gestion des API dans le conteneur spécifié dans un compte de stockage fourni par l’utilisateur|
|/service/certificates/delete|Supprimer le certificat existant|
|/service/certificates/read|Obtenir la liste des certificats ou obtenir les détails du certificat|
|/service/certificates/write|Ajouter un nouveau certificat|
|/service/delete|Supprimer l’instance du service Gestion des API|
|/service/diagnostics/delete|Supprime le diagnostic existant|
|/service/diagnostics/loggers/delete|Supprime le mappage d’un enregistreur d’événements avec un paramètre de diagnostic|
|/service/diagnostics/loggers/read|Obtient la liste des enregistreurs d’événements de diagnostic existants|
|/service/diagnostics/loggers/write|Mappe un enregistreur d’événements à un paramètre de diagnostic|
|/service/diagnostics/read|Obtient la liste des diagnostics ou obtient les détails d’un diagnostic|
|/service/diagnostics/write|Ajoute nouveau diagnostic ou met à jour les détails du diagnostic existant|
|/service/getssotoken/action|Obtient le jeton d’authentification unique qui peut être utilisé pour se connecter au portail hérité du service Gestion des API en tant qu’administrateur|
|/service/groups/delete|Supprimer le groupe existant|
|/service/groups/read|Obtenir la liste des groupes ou obtient les détails d’un groupe|
|/service/groups/users/delete|Supprimer un utilisateur existant d’un groupe existant|
|/service/groups/users/read|Obtenir la liste des utilisateurs du groupe|
|/service/groups/users/write|Ajouter un utilisateur existant à un groupe existant|
|/service/groups/write|Créer un nouveau groupe ou mettre à jour les détails du groupe existant|
|/service/identityProviders/delete|Supprimer le fournisseur d’identité existant|
|/service/identityProviders/read|Obtenir la liste des fournisseurs d’identité ou obtenir les détails du fournisseur d’identité|
|/service/identityProviders/write|Créer un nouveau fournisseur d’identité ou mettre à jour les détails d’un fournisseur d’identité existant|
|/service/locations/networkstatus/read|Obtient l’état de l’accès réseau des ressources dont le service dépend dans l’emplacement|
|/service/loggers/delete|Supprimer l’enregistreur existant|
|/service/loggers/read|Obtenir la liste des enregistreurs ou obtenir les détails d’un enregistreur|
|/service/loggers/write|Ajouter un nouvel enregistreur ou mettre à jour les détails d’un enregistreur existant|
|/service/managedeployments/action|Modifier une référence/unité, ajouter/supprimer des déploiements régionaux du service Gestion des API|
|/service/networkstatus/read|Obtient l’état de l’accès réseau des ressources dont le service dépend|
|/service/notifications/action|Envoie une notification à un utilisateur spécifié|
|/service/notifications/read|Obtient toutes les notifications de l’éditeur Gestion des API ou des détails de notification de l’éditeur Gestion des API|
|/service/notifications/recipientEmails/delete|Supprime un e-mail associé à une notification|
|/service/notifications/recipientEmails/read|Obtient les destinataires associés à une notification par e-mail de l’éditeur Gestion des API|
|/service/notifications/recipientEmails/write|Crée un destinataire de la notification par e-mail|
|/service/notifications/recipientUsers/delete|Supprime l’utilisateur associé aux destinataires de la notification|
|/service/notifications/recipientUsers/read|Obtient les utilisateurs destinataires associés à la notification|
|/service/notifications/recipientUsers/write|Ajoute l’utilisateur aux destinataires de la notification|
|/service/notifications/write|Crée ou met à jour une notification de l’éditeur Gestion des API|
|/service/openidConnectProviders/delete|Supprimer le fournisseur OpenID Connect existant|
|/service/openidConnectProviders/read|Obtenir la liste des fournisseurs OpenID Connect ou obtenir les détails du fournisseur OpenID Connect|
|/service/openidConnectProviders/write|Créer un nouveau fournisseur OpenID Connect ou mettre à jour les détails d’un fournisseur OpenID Connect existant|
|/service/operationresults/read|Obtient l’état actuel d’une opération longue|
|/service/policies/delete|Supprime une configuration de stratégie des stratégies du client|
|/service/policies/read|Obtient les stratégies ou les détails de configuration de stratégie pour le client|
|/service/policies/write|Définit les détails de configuration de stratégie pour le client|
|/service/policySnippets/read|Obtient tous les extraits de code de stratégie|
|/service/portalsettings/read|Obtient les paramètres d’inscription, de connexion ou de délégation pour le portail|
|/service/portalsettings/write|Met à jour les paramètres d’inscription, de connexion ou de délégation|
|/service/products/apis/delete|Supprimer une API existante d’un produit existant|
|/service/products/apis/read|Obtenir la liste des API ajoutées à un produit existant|
|/service/products/apis/write|Ajouter une API existante à un produit existant|
|/service/products/delete|Supprimer un produit existant|
|/service/products/groups/delete|Supprime l’association d’un groupe de développeurs existant à un produit existant|
|/service/products/groups/read|Obtenir la liste des groupes de développeurs associés au produit|
|/service/products/groups/write|Associer un groupe de développeurs existant à un produit existant|
|/service/products/policies/delete|Supprime une configuration de stratégie des stratégies de produit|
|/service/products/policies/read|Obtient les stratégies ou les détails de configuration de stratégie pour un produit|
|/service/products/policies/write|Définit les détails de configuration de stratégie pour un produit|
|/service/products/policy/delete|Supprimer la configuration de stratégie d’un produit existant|
|/service/products/policy/read|Obtenir la configuration de stratégie d’un produit existant|
|/service/products/policy/write|Définir la configuration de stratégie pour un produit existant|
|/service/products/read|Obtenir la liste des produits ou obtenir les détails du produit|
|/service/products/subscriptions/read|Obtenir la liste des abonnements de produit|
|/service/products/tags/delete|Supprime l’association d’une balise existante à un produit existant|
|/service/products/tags/read|Obtient les balises associées au produit ou des détails de balise|
|/service/products/tags/write|Associe une balise existante à un produit existant|
|/service/products/write|Créer un nouveau produit ou mettre à jour des détails du produit existants|
|/service/properties/delete|Supprime la propriété existante|
|/service/properties/read|Obtient la liste de toutes les propriétés ou obtient les détails de la propriété spécifiée|
|/service/properties/write|Crée une nouvelle propriété ou met à jour la valeur de la propriété spécifiée|
|/service/providers/Microsoft.Insights/diagnosticSettings/read|Obtient le paramètre de diagnostic pour le service Gestion des API|
|/service/providers/Microsoft.Insights/diagnosticSettings/write|Crée ou met à jour le paramètre de diagnostic pour le service Gestion des API|
|/service/providers/Microsoft.Insights/logDefinitions/read|Obtient les journaux disponibles pour le service Gestion des API|
|/service/providers/Microsoft.Insights/metricDefinitions/read|Obtient les métriques disponibles pour le service Gestion des API|
|/service/quotas/periods/read|Obtient la valeur de compteur de quota pour une période|
|/service/quotas/periods/write|Définit la valeur actuelle du compteur de quota|
|/service/quotas/read|Obtient les valeurs pour le quota|
|/service/quotas/write|Définit la valeur actuelle du compteur de quota|
|/service/read|Lire les métadonnées d’une instance du service Gestion des API|
|/service/reports/read|Obtient un rapport agrégé par période de temps, par région géographique ou par développeur Ou obtient un rapport agrégé par produit Ou obtient un rapport agrégé par API, par opération ou par abonnement Ou obtient des données pour le rapport de demandes|
|/service/restore/action|Restaurer le service Gestion des API à partir du conteneur spécifié dans un compte de stockage fourni par l’utilisateur|
|/service/subscriptions/delete|Supprimez l’abonnement. Cette opération peut être utilisée pour supprimer l’abonnement|
|/service/subscriptions/read|Obtenir la liste des abonnements de produit ou obtenir les détails de l’abonnement de produit|
|/service/subscriptions/regeneratePrimaryKey/action|Régénérer la clé primaire d’abonnement|
|/service/subscriptions/regenerateSecondaryKey/action|Régénérer la clé secondaire d’abonnement|
|/service/subscriptions/write|Abonnez un utilisateur existant à un produit existant ou mettez à jour les détails de l’abonnement existant. Cette opération peut être utilisée pour renouveler l’abonnement|
|/service/tagResources/read|Obtient la liste des balises avec les ressources associées|
|/service/tags/delete|Supprime la balise existante|
|/service/tags/read|Obtient la liste des balises ou les détails d’une balise|
|/service/tags/write|Ajoute une balise ou met à jour les détails d’une balise existante|
|/service/templates/delete|Réinitialise le modèle d’e-mail par défaut de Gestion des API|
|/service/templates/read|Obtient tous les modèles d’e-mail ou les détails d’un modèle d’e-mail de Gestion des API|
|/service/templates/write|Crée ou met à jour le modèle d’e-mail de Gestion des API|
|/service/tenant/delete|Supprimer la configuration de la stratégie du client|
|/service/tenant/deploy/action|Exécute une tâche de déploiement pour appliquer les modifications de la branche git spécifiée à la configuration dans la base de données.|
|/service/tenant/operationResults/read|Obtenir la liste des résultats d’opération ou obtenir le résultat d’une opération spécifique|
|/service/tenant/read|Obtient la configuration de stratégie pour le client ou les détails des informations d’accès du client|
|/service/tenant/regeneratePrimaryKey/action|Régénérer la clé d’accès primaire|
|/service/tenant/regenerateSecondaryKey/action|Régénérer la clé d’accès secondaire|
|/service/tenant/save/action|Crée une validation avec un instantané de configuration dans la branche spécifiée du référentiel|
|/service/tenant/syncState/read|Obtenir l’état de la dernière synchronisation git|
|/service/tenant/validate/action|Valide les modifications de la branche git spécifiée|
|/service/tenant/write|Définit la configuration de stratégie pour le client ou met à jour les détails des informations d’accès du client|
|/service/updatecertificate/action|Télécharger le certificat SSL pour un service Gestion des API|
|/service/updatehostname/action|Configurer, mettre à jour ou supprimer des noms de domaine personnalisés pour un service Gestion des API|
|/service/users/action|Enregistre un nouvel utilisateur|
|/service/users/applications/attachments/delete|Supprime une pièce jointe|
|/service/users/applications/attachments/read|Obtient les pièces jointes de l’application ou une pièce jointe|
|/service/users/applications/attachments/write|Ajoute une pièce jointe à l’application|
|/service/users/applications/delete|Supprime une application existante|
|/service/users/applications/read|Obtient la liste de toutes les applications de l’utilisateur ou les détails de l’application Gestion des API|
|/service/users/applications/write|Inscrit une application auprès de Gestion des API ou met à jour les détails d’une application|
|/service/users/delete|Supprimer le compte d’utilisateur|
|/service/users/generateSsoUrl/action|Générez l’URL d’authentification unique. L’URL peut être utilisée pour accéder au portail d’administration|
|/service/users/groups/read|Obtenir la liste des groupes d’utilisateurs|
|/service/users/keys/read|Obtenir la liste des clés utilisateur|
|/service/users/read|Obtenir la liste des utilisateurs inscrits ou obtenir les informations de compte d’un utilisateur|
|/service/users/subscriptions/read|Obtenir la liste des abonnements utilisateur|
|/service/users/token/action|Obtient un jeton d’accès pour un utilisateur|
|/service/users/write|Inscrire un nouvel utilisateur ou mettre à jour les informations de compte d’un utilisateur existant|
|/service/write|Créer une instance du service Gestion des API|
|/unregister/action|Annuler l’inscription de l’abonnement pour le fournisseur de ressources Microsoft.ApiManagement|

## <a name="microsoftauthorization"></a>Microsoft.Authorization

| Opération | Description |
|---|---|
|/checkAccess/action|Vérifie si l’appelant est autorisé à effectuer une action particulière|
|/classicAdministrators/delete|Supprime l’administrateur de l’abonnement.|
|/classicAdministrators/read|Lit les administrateurs de l’abonnement.|
|/classicAdministrators/write|Ajoutez ou modifiez un administrateur à un abonnement.|
|/elevateAccess/action|Accorde à l’appelant un accès Administrateur de l’accès utilisateur au niveau de la portée du client|
|/locks/delete|Supprime des verrous au niveau de la portée spécifiée.|
|/locks/read|Obtient des verrous au niveau de la portée spécifiée.|
|/locks/write|Ajoute des verrous au niveau de la portée spécifiée.|
|/permissions/read|Répertorie toutes les autorisations dont dispose l’appelant au niveau d’une portée donnée.|
|/policyAssignments/delete|Supprimez une affectation de stratégie au niveau de la portée spécifiée.|
|/policyAssignments/read|Obtenez des informations sur une affectation de stratégie.|
|/policyAssignments/write|Créez une affectation de stratégie au niveau de la portée spécifiée.|
|/policyDefinitions/delete|Supprimez une définition de stratégie.|
|/policyDefinitions/read|Obtenez des informations sur une définition de stratégie.|
|/policyDefinitions/write|Créez une définition de stratégie personnalisée.|
|/policySetDefinitions/delete|Supprime une définition d’ensemble de stratégies|
|/policySetDefinitions/read|Obtient des informations sur une définition d’ensemble de stratégies|
|/policySetDefinitions/write|Crée une définition d’ensemble de stratégies personnalisé|
|/providerOperations/read|Obtenez des opérations pour tous les fournisseurs de ressources qui peuvent être utilisées dans les définitions de rôles.|
|/roleAssignments/delete|Supprimez une affectation de rôle au niveau de la portée spécifiée.|
|/roleAssignments/read|Obtenez des informations sur une affectation de rôle.|
|/roleAssignments/write|Créez une affectation de rôle au niveau de la portée spécifiée.|
|/roleDefinitions/delete|Supprimez la définition de rôle personnalisé spécifiée.|
|/roleDefinitions/read|Obtenez des informations sur une définition de rôle.|
|/roleDefinitions/write|Créez ou mettez à jour une définition de rôle personnalisé avec des autorisations spécifiées et des portées pouvant être affectées.|

## <a name="microsoftautomation"></a>Microsoft.Automation

| Opération | Description |
|---|---|
|/automationAccounts/agentRegistrationInformation/read|Lit les informations d’inscription d’Azure Automation DSC|
|/automationAccounts/agentRegistrationInformation/regenerateKey/action|Écrit une demande de régénération de clés Azure Automation DSC|
|/automationAccounts/certificates/delete|Supprime une ressource de certificat Azure Automation|
|/automationAccounts/certificates/read|Obtient une ressource de certificat Azure Automation|
|/automationAccounts/certificates/write|Crée ou met à jour une ressource de certificat Azure Automation|
|/automationAccounts/compilationjobs/read|Lit une compilation d’Azure Automation DSC|
|/automationAccounts/compilationjobs/write|Écrit une compilation d’Azure Automation DSC|
|/automationAccounts/configurations/delete|Supprime un contenu d’Azure Automation DSC|
|/automationAccounts/configurations/getCount/action|Lit le nombre d’un contenu d’Azure Automation DSC|
|/automationAccounts/configurations/read|Obtient un contenu d’Azure Automation DSC|
|/automationAccounts/configurations/write|Écrit un contenu d’Azure Automation DSC|
|/automationAccounts/connections/delete|Supprime une ressource de connexion Azure Automation|
|/automationAccounts/connections/read|Obtient une ressource de connexion Azure Automation|
|/automationAccounts/connections/write|Crée ou met à jour une ressource de connexion Azure Automation|
|/automationAccounts/connectionTypes/delete|Supprime une ressource de type de connexion Azure Automation|
|/automationAccounts/connectionTypes/read|Obtient une ressource de type de connexion Azure Automation|
|/automationAccounts/connectionTypes/write|Crée une ressource de type de connexion Azure Automation|
|/automationAccounts/credentials/delete|Supprime une ressource d’information d’identification Azure Automation|
|/automationAccounts/credentials/read|Obtient une ressource d’information d’identification Azure Automation|
|/automationAccounts/credentials/write|Crée ou met à jour une ressource d’information d’identification Azure Automation|
|/automationAccounts/delete|Supprime un compte Azure Automation|
|/automationAccounts/diagnosticSettings/read|Obtient le paramètre de diagnostic pour la ressource|
|/automationAccounts/diagnosticSettings/write|Obtient le paramètre de diagnostic pour la ressource|
|/automationAccounts/hybridRunbookWorkerGroups/delete|Supprime des ressources Runbook Worker hybrides|
|/automationAccounts/hybridRunbookWorkerGroups/read|Lit des ressources Runbook Worker hybrides|
|/automationAccounts/jobs/output/action|Obtient le résultat d’un travail|
|/automationAccounts/jobs/output/action|Obtient le résultat d’un travail|
|/automationAccounts/jobs/read|Obtient un travail Azure Automation|
|/automationAccounts/jobs/read|Obtient un travail Azure Automation|
|/automationAccounts/jobs/resume/action|Reprend un travail Azure Automation|
|/automationAccounts/jobs/resume/action|Reprend un travail Azure Automation|
|/automationAccounts/jobs/runbookContent/action|Obtient le contenu du runbook Azure Automation au moment de l’exécution du travail|
|/automationAccounts/jobs/runbookContent/action|Obtient le contenu du runbook Azure Automation au moment de l’exécution du travail|
|/automationAccounts/jobs/stop/action|Arrête un travail Azure Automation|
|/automationAccounts/jobs/stop/action|Arrête un travail Azure Automation|
|/automationAccounts/jobs/streams/read|Obtient un flux de travail Azure Automation|
|/automationAccounts/jobs/streams/read|Obtient un flux de travail Azure Automation|
|/automationAccounts/jobs/suspend/action|Suspend un travail Azure Automation|
|/automationAccounts/jobs/suspend/action|Suspend un travail Azure Automation|
|/automationAccounts/jobs/write|Crée un travail Azure Automation|
|/automationAccounts/jobs/write|Crée un travail Azure Automation|
|/automationAccounts/jobSchedules/delete|Supprime une planification du travail Azure Automation|
|/automationAccounts/jobSchedules/read|Obtient une planification du travail Azure Automation|
|/automationAccounts/jobSchedules/write|Crée une planification du travail Azure Automation|
|/automationAccounts/linkedWorkspace/read|Obtient l’espace de travail lié au compte Automation|
|/automationAccounts/logDefinitions/read|Obtient les journaux disponibles pour le compte Automation|
|/automationAccounts/modules/activities/read|Obtient les activités d’Azure Automation|
|/automationAccounts/modules/delete|Supprime un module Azure Automation|
|/automationAccounts/modules/read|Obtient un module Azure Automation|
|/automationAccounts/modules/write|Crée ou met à jour un module Azure Automation|
|/automationAccounts/nodeConfigurations/delete|Supprime une configuration de nœud d’Azure Automation DSC|
|/automationAccounts/nodeConfigurations/read|Lit une configuration de nœud d’Azure Automation DSC|
|/automationAccounts/nodeConfigurations/readContent/action|Lit le contenu d’une configuration de nœud d’Azure Automation DSC|
|/automationAccounts/nodeConfigurations/write|Écrit une configuration de nœud d’Azure Automation DSC|
|/automationAccounts/nodes/delete|Supprime des nœuds Azure Automation DSC|
|/automationAccounts/nodes/read|Lit des nœuds Azure Automation DSC|
|/automationAccounts/nodes/reports/read|Lit le contenu d’un rapport Azure Automation DSC|
|/automationAccounts/nodes/reports/read|Lit un rapport Azure Automation DSC|
|/automationAccounts/objectDataTypes/fields/read|Obtient les TypeFields Azure Automation|
|/automationAccounts/providers/Microsoft.Insights/metricDefinitions/read|Obtient les définitions de métrique d’Automation|
|/automationAccounts/read|Obtient un compte Azure Automation|
|/automationAccounts/runbooks/delete|Supprime un runbook Azure Automation|
|/automationAccounts/runbooks/draft/publish/action|Publie un brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/read|Obtient un brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/readContent/action|Obtient le contenu d’un brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/testJob/read|Obtient un travail de test de brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/testJob/resume/action|Reprend un travail de test de brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/testJob/stop/action|Arrête un travail de test de brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/testJob/suspend/action|Suspend un travail de test de brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/testJob/write|Crée un travail de test de brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/undoEdit/action|Annule les modifications apportées à un brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/draft/writeContent/action|Crée le contenu d’un brouillon de runbook Azure Automation|
|/automationAccounts/runbooks/read|Obtient un runbook Azure Automation|
|/automationAccounts/runbooks/readContent/action|Obtient le contenu d’un runbook Azure Automation|
|/automationAccounts/runbooks/write|Crée ou met à jour un runbook Azure Automation|
|/automationAccounts/schedules/delete|Supprime une ressource de planification Azure Automation|
|/automationAccounts/schedules/read|Obtient une ressource de planification Azure Automation|
|/automationAccounts/schedules/write|Crée ou met à jour une ressource de planification Azure Automation|
|/automationAccounts/statistics/read|Obtient les statistiques d’Azure Automation|
|/automationAccounts/usages/read|Obtient l’utilisation d’Azure Automation|
|/automationAccounts/variables/delete|Supprime une ressource de variable Azure Automation|
|/automationAccounts/variables/read|Lit une ressource de variable Azure Automation|
|/automationAccounts/variables/write|Crée ou met à jour une ressource de variable Azure Automation|
|/automationAccounts/watchers/streams/read|Obtient un flux de tâches Automation Watcher Azure|
|/automationAccounts/webhooks/delete|Supprime un webhook Azure Automation |
|/automationAccounts/webhooks/generateUri/action|Génère un URI pour un webhook Azure Automation|
|/automationAccounts/webhooks/read|Lit un webhook Azure Automation|
|/automationAccounts/webhooks/write|Crée ou met à jour un webhook Azure Automation|
|/automationAccounts/write|Crée ou met à jour un compte Azure Automation|
|/automationAccounts/write|Crée ou met à jour un compte Azure Automation|

## <a name="microsoftazureactivedirectory"></a>Microsoft.AzureActiveDirectory

| Opération | Description |
|---|---|
|/b2cDirectories/delete|Supprime une ressource de répertoire B2C|
|/b2cDirectories/read|Affiche une ressource de répertoire B2C|
|/b2cDirectories/write|Crée ou met à jour une ressource de répertoire B2C|
|/operations/read|Lit toutes les opérations d’API disponibles pour le fournisseur de ressources Microsoft.AzureActiveDirectory|
|/register/action|Enregistre l’abonnement à un fournisseur de ressources Microsoft.AzureActiveDirectory|

## <a name="microsoftazurestack"></a>Microsoft.AzureStack

| Opération | Description |
|---|---|
|/Operations/read|Obtient les propriétés d’une opération de fournisseur de ressources|
|/register/action|Inscrit l’abonnement auprès du fournisseur de ressources Microsoft.AzureStack|
|/registrations/customerSubscriptions/delete|Supprime un abonnement client Azure Stack|
|/registrations/customerSubscriptions/read|Obtient les propriétés d’un abonnement client Azure Stack|
|/registrations/customerSubscriptions/write|Crée ou met à jour un abonnement client Azure Stack|
|/registrations/delete|Vérifie une inscription Azure Stack|
|/registrations/getActivationKey/action|Obtient la dernière clé d’activation Azure Stack|
|/registrations/products/listDetails/action|Récupère les détails étendus d’un produit de la place de marché Azure Stack|
|/registrations/products/read|Obtient les propriétés d’un produit de la place de marché Azure Stack|
|/registrations/read|Obtient les propriétés d’une inscription Azure Stack|
|/registrations/write|Crée ou met à jour une inscription Azure Stack|

## <a name="microsoftbatch"></a>Microsoft.Batch

| Opération | Description |
|---|---|
|/batchAccounts/applications/delete|Supprime une application|
|/batchAccounts/applications/read|Répertorie les applications ou obtient les propriétés d’une application|
|/batchAccounts/applications/versions/activate/action|Active un package d’application|
|/batchAccounts/applications/versions/delete|Supprime un package d’application|
|/batchAccounts/applications/versions/read|Obtient les propriétés d’un package d’application|
|/batchAccounts/applications/versions/write|Crée une nouveau package d’application ou met à jour un package d’application existant|
|/batchAccounts/applications/write|Crée une nouvelle application ou met à jour une application existante|
|/batchAccounts/certificateOperationResults/read|Obtient les résultats d’une opération de certificat de longue durée sur un compte Batch|
|/batchAccounts/certificates/cancelDelete/action|Annule la suppression manquée d’un certificat sur un compte Batch|
|/batchAccounts/certificates/delete|Supprime un certificat d’un compte Batch|
|/batchAccounts/certificates/read|Répertorie les certificats sur un compte Batch ou obtient les propriétés d’un certificat|
|/batchAccounts/certificates/write|Crée un certificat sur un compte Batch ou met à jour un certificat existant|
|/batchAccounts/delete|Supprime un compte Batch|
|/batchAccounts/listkeys/action|Répertorie les clés d’accès pour un compte Batch|
|/batchAccounts/operationResults/read|Obtient les résultats d’une opération de compte Batch de longue durée|
|/batchAccounts/poolOperationResults/read|Obtient les résultats d’une opération de pool de longue durée sur un compte Batch|
|/batchAccounts/pools/delete|Supprime un pool d’un compte Batch|
|/batchAccounts/pools/disableAutoscale/action|Désactive la mise à l’échelle automatique pour un pool de comptes Batch|
|/batchAccounts/pools/read|Répertorie les pools sur un compte Batch ou obtient les propriétés d’un pool|
|/batchAccounts/pools/stopResize/action|Arrête une opération de redimensionnement en cours sur un pool de comptes Batch|
|/batchAccounts/pools/upgradeOs/action|Met à niveau le système d’exploitation d’un pool de comptes Batch|
|/batchAccounts/pools/write|Crée un pool sur un compte Batch ou met à jour un pool existant|
|/batchAccounts/providers/Microsoft.Insights/diagnosticSettings/read|Obtient le paramètre de diagnostic pour la ressource|
|/batchAccounts/providers/Microsoft.Insights/diagnosticSettings/write|Crée ou met à jour le paramètre de diagnostic pour la ressource|
|/batchAccounts/providers/Microsoft.Insights/logDefinitions/read|Obtient les journaux disponibles pour le service Batch|
|/batchAccounts/providers/Microsoft.Insights/metricDefinitions/read|Obtient les métriques disponibles pour le service Batch|
|/batchAccounts/read|Répertorie les comptes Batch ou obtient les propriétés d’un compte Batch|
|/batchAccounts/regeneratekeys/action|Régénère les clés d’accès pour un compte Batch|
|/batchAccounts/syncAutoStorageKeys/action|Synchronise les clés d’accès pour le compte de stockage automatique configuré pour un compte Batch|
|/batchAccounts/write|Crée un nouveau compte Batch ou met à jour un compte Batch existant|
|/locations/checkNameAvailability/action|Vérifie que le nom de compte est valide et qu’il n’est pas utilisé|
|/locations/quotas/read|Obtient les quotas Batch de l’abonnement spécifié au niveau de la région Azure spécifiée|
|/register/action|Inscrit l’abonnement pour le fournisseur de ressources Batch et permet la création de comptes Batch|
|/unregister/action|Désinscrit l’abonnement pour le fournisseur de ressources Batch en empêchant la création de comptes Batch|

## <a name="microsoftbatchai"></a>Microsoft.BatchAI

| Opération | Description |
|---|---|
|/clusters/delete|Supprime un cluster Batch AI|
|/clusters/read|Répertorie les clusters Batch AI ou obtient les propriétés d’un cluster Batch AI|
|/clusters/remoteLoginInformation/action|Répertorie les informations de connexion à distance pour un cluster Batch AI|
|/clusters/write|Crée un cluster Batch AI ou met à jour un cluster Batch AI existant|
|/fileservers/delete|Supprime un serveur de fichiers Batch AI|
|/fileservers/read|Répertorie les serveurs de fichiers Batch AI ou obtient les propriétés d’un serveur de fichiers Batch AI|
|/fileservers/resume/action|Reprend l’exécution d’un serveur de fichiers Batch AI|
|/fileservers/suspend/action|Interrompt un serveur de fichiers Batch AI|
|/fileservers/write|Crée ou met à jour un serveur de fichiers Batch AI|
|/jobs/delete|Supprime une tâche Batch AI|
|/jobs/read|Répertorie les tâches Batch AI ou obtient les propriétés d’une tâche Batch AI|
|/jobs/remoteLoginInformation/action|Affiche les informations de connexion à distance pour une tâche Batch AI|
|/jobs/terminate/action|Met fin à une tâche Batch AI|
|/jobs/write|Crée ou met à jour une tâche Batch AI|
|/register/action|Inscrit l’abonnement pour le fournisseur de ressources Batch AI et permet la création de ressources Batch AI|

## <a name="microsoftbilling"></a>Microsoft.Billing

| Opération | Description |
|---|---|
|/billingPeriods/read|Répertorie les périodes de facturation disponibles|
|/invoices/read|Répertorie les factures disponibles|

## <a name="microsoftbingmaps"></a>Microsoft.BingMaps

| Opération | Description |
|---|---|
|/mapApis/Delete|Opération de suppression|
|/mapApis/listSecrets/action|Répertorie les secrets|
|/mapApis/listSingleSignOnToken/action|Lire le jeton d’autorisation d’authentification unique pour la ressource|
|/mapApis/Read|Opération de lecture|
|/mapApis/regenerateKey/action|Régénère la clé|
|/mapApis/Write|Opération d’écriture|
|/Operations/read|Description de l’opération.|

## <a name="microsoftcache"></a>Microsoft.Cache

| Opération | Description |
|---|---|
|/checknameavailability/action|Vérifie si un nom peut être utilisé avec un nouveau cache Redis|
|/operations/read|Répertorie les opérations que le fournisseur Microsoft.Cache prend en charge.|
|/redis/delete|Supprimer l’intégralité du cache Redis|
|/redis/export/action|Exporter des données Redis vers des objets blob préfixés dans un format spécifié|
|/redis/firewallRules/delete|Supprimer des règles de pare-feu IP d’un cache Redis|
|/redis/firewallRules/read|Obtenir les règles de pare-feu IP d’un cache Redis|
|/redis/firewallRules/write|Modifier les règles de pare-feu IP d’un cache Redis|
|/redis/forceReboot/action|Forcez le redémarrage d’instance de cache, potentiellement avec une perte de données.|
|/redis/import/action|Importer des données d’un format spécifié à partir de plusieurs objets blob dans Redis|
|/redis/linkedservers/delete|Supprimer un serveur lié d’un cache Redis|
|/redis/linkedservers/read|Obtenez les serveurs liés associés à un cache Redis.|
|/redis/linkedservers/write|Ajouter un serveur lié à un cache Redis|
|/redis/listKeys/action|Afficher la valeur des clés d’accès du cache Redis dans le portail de gestion|
|/redis/listUpgradeNotifications/read|Répertoriez les dernières notifications de mise à niveau du client de cache.|
|/redis/locations/operationresults/read|Obtient le résultat d’une opération de longue durée pour laquelle l’en-tête Location a été précédemment retourné au client|
|/redis/metricDefinitions/read|Obtient les mesures disponibles pour un cache Redis|
|/redis/patchSchedules/delete|Supprimer la planification de correctif d’un cache Redis|
|/redis/patchSchedules/read|Obtient la planification de mise à jour corrective d’un cache Redis|
|/redis/patchSchedules/write|Modifier la planification de mise à jour corrective d’un cache Redis|
|/redis/read|Afficher les paramètres et la configuration du cache Redis dans le portail de gestion|
|/redis/regenerateKey/action|Modifier la valeur des clés d’accès du cache Redis dans le portail de gestion|
|/redis/start/action|Démarrez une instance de cache.|
|/redis/stop/action|Arrêtez une instance de cache.|
|/redis/write|Modifier les paramètres et la configuration du cache Redis dans le portail de gestion|
|/register/action|Inscrit le fournisseur de ressources « Microsoft.Cache » à un abonnement|
|/unregister/action|Annule l’inscription du fournisseur de ressources « Microsoft.Cache » à un abonnement|

## <a name="microsoftcapacity"></a>Microsoft.Capacity

| Opération | Description |
|---|---|
|/register/action|Inscrit le fournisseur de ressources de capacité et active la création de ressources de capacité.|
|/reservationorders/action|Met à jour une réservation|
|/reservationorders/delete|Supprime une réservation|
|/reservationorders/read|Lit toutes les réservations|
|/reservationorders/reservations/action|Met à jour une réservation|
|/reservationorders/reservations/delete|Supprime une réservation|
|/reservationorders/reservations/read|Lit toutes les réservations|
|/reservationorders/reservations/revisions/read|Lit toutes les réservations|
|/reservationorders/reservations/write|Crée une réservation|
|/reservationorders/write|Crée une réservation|

## <a name="microsoftcdn"></a>Microsoft.Cdn

| Opération | Description |
|---|---|
|/CheckNameAvailability/action||
|/CheckResourceUsage/action||
|/edgenodes/delete||
|/edgenodes/read||
|/edgenodes/write||
|/operationresults/delete||
|/operationresults/profileresults/CheckResourceUsage/action||
|/operationresults/profileresults/delete||
|/operationresults/profileresults/endpointresults/CheckResourceUsage/action||
|/operationresults/profileresults/endpointresults/customdomainresults/delete||
|/operationresults/profileresults/endpointresults/customdomainresults/ DisableCustomHttps/action||
|/operationresults/profileresults/endpointresults/customdomainresults/ EnableCustomHttps/action||
|/operationresults/profileresults/endpointresults/customdomainresults/read||
|/operationresults/profileresults/endpointresults/customdomainresults/write||
|/operationresults/profileresults/endpointresults/delete||
|/operationresults/profileresults/endpointresults/Load/action||
|/operationresults/profileresults/endpointresults/originresults/delete||
|/operationresults/profileresults/endpointresults/originresults/read||
|/operationresults/profileresults/endpointresults/originresults/write||
|/operationresults/profileresults/endpointresults/Purge/action||
|/operationresults/profileresults/endpointresults/read||
|/operationresults/profileresults/endpointresults/Start/action||
|/operationresults/profileresults/endpointresults/Stop/action||
|/operationresults/profileresults/endpointresults/ValidateCustomDomain/action||
|/operationresults/profileresults/endpointresults/write||
|/operationresults/profileresults/GenerateSsoUri/action||
|/operationresults/profileresults/GetSupportedOptimizationTypes/action||
|/operationresults/profileresults/read||
|/operationresults/profileresults/write||
|/operationresults/read||
|/operationresults/write||
|/operations/read||
|/profiles/CheckResourceUsage/action||
|/profiles/delete||
|/profiles/endpoints/CheckResourceUsage/action||
|/profiles/endpoints/customdomains/delete||
|/profiles/endpoints/customdomains/DisableCustomHttps/action||
|/profiles/endpoints/customdomains/EnableCustomHttps/action||
|/profiles/endpoints/customdomains/read||
|/profiles/endpoints/customdomains/write||
|/profiles/endpoints/delete||
|/profiles/endpoints/Load/action||
|/profiles/endpoints/origins/delete||
|/profiles/endpoints/origins/read||
|/profiles/endpoints/origins/write||
|/profiles/endpoints/providers/Microsoft.Insights/diagnosticSettings/read|Obtient les paramètres de diagnostic pour la ressource|
|/profiles/endpoints/providers/Microsoft.Insights/diagnosticSettings/write|Crée ou met à jour les paramètres de diagnostic pour la ressource|
|/profiles/endpoints/providers/Microsoft.Insights/logDefinitions/read|Obtient les journaux disponibles pour Microsoft.Cdn|
|/profiles/endpoints/Purge/action||
|/profiles/endpoints/read||
|/profiles/endpoints/Start/action||
|/profiles/endpoints/Stop/action||
|/profiles/endpoints/ValidateCustomDomain/action||
|/profiles/endpoints/write||
|/profiles/GenerateSsoUri/action||
|/profiles/GetSupportedOptimizationTypes/action||
|/profiles/read||
|/profiles/write||
|/register/action|Inscrit l’abonnement pour le fournisseur de ressources CDN et active la création de profils CDN|
|/ValidateProbe/action||

## <a name="microsoftcertificateregistration"></a>Microsoft.CertificateRegistration

| Opération | Description |
|---|---|
|/certificateOrders/certificates/Delete|Supprimer un certificat existant|
|/certificateOrders/certificates/Read|Obtenir la liste des certificats|
|/certificateOrders/certificates/Write|Ajouter un nouveau certificat ou en mettre un existant à jour|
|/certificateOrders/Delete|Supprimer un AppServiceCertificate existant|
|/certificateOrders/operations/Read|Liste de toutes les opérations de l’enregistrement de certificat de service d’application|
|/certificateOrders/Read|Obtenir la liste des CertificateOrders|
|/certificateOrders/reissue/Action|Réémettre un certificateorder existant|
|/certificateOrders/renew/Action|Renouveler un certificateorder existant|
|/certificateOrders/resendEmail/Action|Renvoyer l’e-mail de certificat|
|/certificateOrders/resendRequestEmails/Action|Renvoyer des e-mails de demande à une autre adresse de messagerie|
|/certificateOrders/resendRequestEmails/Action|Récupérer le Seal de site pour un App Service Certificate émis|
|/certificateOrders/retrieveCertificateActions/Action|Récupérer la liste des actions de certificat|
|/certificateOrders/retrieveEmailHistory/Action|Récupérer l’historique d’e-mails de certificat|
|/certificateOrders/verifyDomainOwnership/Action|Vérifier la propriété du domaine|
|/certificateOrders/Write|Ajouter un nouveau certificateOrder ou en mettre un existant à jour|
|/provisionGlobalAppServicePrincipalInUserTenant/Action|Approvisionner le principal de service pour un principal d’application de service|
|/register/action|Inscrire le fournisseur de ressources de certificats Microsoft pour l’abonnement|
|/validateCertificateRegistrationInformation/Action|Valider l’objet d’achat de certificat sans le soumettre|

## <a name="microsoftclassiccompute"></a>Microsoft.ClassicCompute

| Opération | Description |
|---|---|
|/capabilities/read|Affiche les fonctionnalités|
|/checkDomainNameAvailability/action|Vérifie la disponibilité d’un nom de domaine donné.|
|/domainNames/active/write|Définit le nom de domaine actif.|
|/domainNames/availabilitySets/read|Affichez le groupe à haute disponibilité de la ressource.|
|/domainNames/capabilities/read|Affiche les fonctionnalités de nom de domaine|
|/domainNames/delete|Supprimez les noms de domaine pour les ressources.|
|/domainNames/extensions/delete|Supprimez les extensions de nom de domaine.|
|/domainNames/extensions/operationStatuses/read|Lit l’état de l’opération pour les extensions de noms de domaine.|
|/domainNames/extensions/read|Retourne les extensions de nom de domaine.|
|/domainNames/extensions/write|Ajoutez les extensions de nom de domaine.|
|/domainNames/internalLoadBalancers/delete|Supprimez un nouvel équilibrage de charge interne.|
|/domainNames/internalLoadBalancers/operationStatuses/read|Lit l’état de l’opération pour les équilibreurs de charge interne de noms de domaine.|
|/domainNames/internalLoadBalancers/read|Obtient les équilibreurs de charge interne.|
|/domainNames/internalLoadBalancers/write|Crée un nouvel équilibrage de charge interne.|
|/domainNames/loadBalancedEndpointSets/operationStatuses/read|Lit l’état de l’opération pour les ensembles de points de terminaison à charge équilibrée de noms de domaine.|
|/domainNames/loadBalancedEndpointSets/read|Affiche les ensembles de points de terminaison à charge équilibrée|
|/domainNames/read|Retournez les noms de domaine pour les ressources.|
|/domainNames/serviceCertificates/delete|Supprimez les certificats de service utilisés.|
|/domainNames/serviceCertificates/operationStatuses/read|Lit l’état de l’opération pour les certificats de service de noms de domaine.|
|/domainNames/serviceCertificates/read|Retourne les certificats de service utilisés.|
|/domainNames/serviceCertificates/write|Ajoutez ou modifiez les certificats de service utilisés.|
|/domainNames/slots/delete|Supprime un emplacement de déploiement donné.|
|/domainNames/slots/operationStatuses/read|Lit l’état de l’opération pour les emplacements de noms de domaine.|
|/domainNames/slots/read|Affiche les emplacements de déploiement.|
|/domainNames/slots/roles/extensionReferences/delete|Supprimez la référence d’extension pour le rôle d’emplacement de déploiement.|
|/domainNames/slots/roles/extensionReferences/operationStatuses/read|Lit l’état de l’opération pour les références d’extension de rôles d’emplacements de noms de domaine.|
|/domainNames/slots/roles/extensionReferences/read|Retourne la référence d’extension pour le rôle d’emplacement de déploiement.|
|/domainNames/slots/roles/extensionReferences/write|Ajoutez ou modifiez la référence d’extension pour le rôle d’emplacement de déploiement.|
|/domainNames/slots/roles/providers/Microsoft.Insights/diagnosticSettings/read|Obtient les paramètres des diagnostics.|
|/domainNames/slots/roles/providers/Microsoft.Insights/diagnosticSettings/write|Ajoutez ou modifiez des paramètres de diagnostics.|
|/domainNames/slots/roles/providers/Microsoft.Insights/metricDefinitions/read|Obtient les définitions de mesures.|
|/domainNames/slots/roles/read|Obtenez le rôle de l’emplacement de déploiement.|
|/domainNames/slots/roles/roleInstances/operationStatuses/read|Lit l’état de l’opération pour les instances de rôle de rôles d’emplacements de noms de domaine.|
|/domainNames/slots/roles/roleInstances/read|Obtenez l’instance de rôle.|
|/domainNames/slots/roles/roleInstances/rebuild/action|Regénère l’instance de rôle|
|/domainNames/slots/roles/roleInstances/reimage/action|Réinitialise l’instance de rôle.|
|/domainNames/slots/roles/roleInstances/restart/action|Redémarre des instances de rôle.|
|/domainNames/slots/start/action|Démarre un emplacement de déploiement.|
|/domainNames/slots/state/start/write|Modifie l’état d’emplacement de déploiement sur arrêté.|
|/domainNames/slots/state/stop/write|Modifie l’état d’emplacement de déploiement sur démarré.|
|/domainNames/slots/stop/action|Suspend l’emplacement de déploiement.|
|/domainNames/slots/upgradeDomain/write|Parcourez la mise à niveau du domaine.|
|/domainNames/slots/write|Crée ou met à jour le déploiement.|
|/domainNames/swap/action|Permute l’emplacement intermédiaire vers l’emplacement de production.|
|/domainNames/write|Ajoutez ou modifiez les noms de domaine pour les ressources.|
|/moveSubscriptionResources/action|Déplacez toutes les ressources classiques vers un autre abonnement.|
|/operatingSystemFamilies/read|Répertorie les familles de systèmes d’exploitation invités disponibles dans Microsoft Azure ainsi que les versions de système d’exploitation disponibles pour chaque famille|
|/operatingSystems/read|Répertorie les versions de système d’exploitation invité qui sont actuellement disponibles dans Microsoft Azure.|
|/quotas/read|Obtient le quota de l’abonnement.|
|/register/action|S’inscrire à Classic Compute|
|/resourceTypes/skus/read|Obtient la liste des références (SKU) pour les types de ressources pris en charge.|
|/validateSubscriptionMoveAvailability/action|Validez la disponibilité de l’abonnement pour l’opération de déplacement classique.|
|/virtualMachines/associatedNetworkSecurityGroups/delete|Supprime le groupe de sécurité réseau associé à la machine virtuelle.|
|/virtualMachines/associatedNetworkSecurityGroups/operationStatuses/read|Lit l’état de l’opération pour les machines virtuelles associées à des groupes de sécurité réseau.|
|/virtualMachines/associatedNetworkSecurityGroups/read|Obtient le groupe de sécurité réseau associé à la machine virtuelle.|
|/virtualMachines/associatedNetworkSecurityGroups/write|Ajoute un groupe de sécurité réseau associé à la machine virtuelle.|
|/virtualMachines/asyncOperations/read|Obtient les opérations asynchrones possibles|
|/virtualMachines/attachDisk/action|Attache un disque de données à une machine virtuelle.|
|/virtualMachines/delete|Supprime des machines virtuelles.|
|/virtualMachines/detachDisk/action|Détache un disque de données d’une machine virtuelle.|
|/virtualMachines/disks/read|Récupère la liste des disques de données|
|/virtualMachines/downloadRemoteDesktopConnectionFile/action|Télécharge le fichier RDP pour la machine virtuelle.|
|/virtualMachines/extensions/operationStatuses/read|Lit l’état de l’opération pour les extensions de machines virtuelles.|
|/virtualMachines/extensions/read|Obtient l’extension de machine virtuelle.|
|/virtualMachines/extensions/write|Place l’extension de machine virtuelle.|
|/virtualMachines/metrics/read|Obtient les mesures.|
|/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/delete|Supprime le groupe de sécurité réseau associé à l’interface réseau.|
|/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/ operationStatuses/read|Lit l’état de l’opération pour les machines virtuelles associées à des groupes de sécurité réseau.|
|/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/read|Obtient le groupe de sécurité réseau associé à l’interface réseau.|
|/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/write|Ajoute un groupe de sécurité réseau associé à l’interface réseau.|
|/virtualMachines/operationStatuses/read|Lit l’état de l’opération pour les machines virtuelles.|
|/virtualMachines/performMaintenance/action|Effectue la maintenance de la machine virtuelle|
|/virtualMachines/providers/Microsoft.Insights/diagnosticSettings/read|Obtient les paramètres des diagnostics.|
|/virtualMachines/providers/Microsoft.Insights/diagnosticSettings/write|Ajoutez ou modifiez des paramètres de diagnostics.|
|/virtualMachines/providers/Microsoft.Insights/metricDefinitions/read|Obtient les définitions de mesures.|
|/virtualMachines/read|Récupère la liste des machines virtuelles.|
|/virtualMachines/redeploy/action|Redéploie la machine virtuelle.|
|/virtualMachines/restart/action|Redémarre des machines virtuelles.|
|/virtualMachines/shutdown/action|Arrêtez la machine virtuelle.|
|/virtualMachines/start/action|Démarrez la machine virtuelle.|
|/virtualMachines/stop/action|Arrête la machine virtuelle.|
|/virtualMachines/write|Ajouter ou modifier des machines virtuelles.|

## <a name="microsoftclassicnetwork"></a>Microsoft.ClassicNetwork

| Opération | Description |
|---|---|
|/gatewaySupportedDevices/read|Récupère la liste des appareils pris en charge.|
|/networkSecurityGroups/delete|Supprime le groupe de sécurité réseau.|
|/networkSecurityGroups/operationStatuses/read|Lit l’état de l’opération pour le groupe de sécurité réseau.|
|/networkSecurityGroups/read|Obtient le groupe de sécurité réseau.|
|/networkSecurityGroups/securityRules/delete|Supprime la règle de sécurité.|
|/networkSecurityGroups/securityRules/operationStatuses/read|Lit l’état de l’opération pour les règles de sécurité du groupe de sécurité réseau.|
|/networkSecurityGroups/securityRules/read|Obtient la règle de sécurité.|
|/networkSecurityGroups/securityRules/write|Ajoute ou met à jour une règle de sécurité.|
|/networkSecurityGroups/write|Ajoute un nouveau groupe de sécurité réseau.|
|/quotas/read|Obtient le quota de l’abonnement.|
|/register/action|S’inscrire à un réseau classique|
|/reservedIps/delete|Supprimez une adresse IP réservée.|
|/reservedIps/join/action|Joindre une adresse IP réservée|
|/reservedIps/link/action|Lier une adresse IP réservée|
|/reservedIps/operationStatuses/read|Lit l’état de l’opération pour les adresses IP réservées.|
|/reservedIps/read|Obtient les adresses IP réservées|
|/reservedIps/write|Ajouter une nouvelle adresse IP réservée|
|/virtualNetworks/capabilities/read|Affiche les fonctionnalités|
|/virtualNetworks/checkIPAddressAvailability/action|Vérifie la disponibilité d’une adresse IP donnée dans un réseau virtuel.|
|/virtualNetworks/delete|Supprime le réseau virtuel.|
|/virtualNetworks/gateways/clientRevokedCertificates/delete|Annule la révocation d’un certificat client.|
|/virtualNetworks/gateways/clientRevokedCertificates/read|Lisez les certificats clients révoqués.|
|/virtualNetworks/gateways/clientRevokedCertificates/write|Révoque un certificat client.|
|/virtualNetworks/gateways/clientRootCertificates/delete|Supprime le certificat client de passerelle de réseau virtuel.|
|/virtualNetworks/gateways/clientRootCertificates/download/action|Télécharge le certificat par empreinte.|
|/virtualNetworks/gateways/clientRootCertificates/listPackage/action|Répertorie le package de certificat de passerelle de réseau virtuel.|
|/virtualNetworks/gateways/clientRootCertificates/read|Recherchez les certificats racine client.|
|/virtualNetworks/gateways/clientRootCertificates/write|Télécharge un nouveau certificat racine client.|
|/virtualNetworks/gateways/connections/connect/action|Établit une connexion de passerelle site à site.|
|/virtualNetworks/gateways/connections/disconnect/action|Déconnecte une connexion de passerelle site à site.|
|/virtualNetworks/gateways/connections/read|Récupère la liste des connexions.|
|/virtualNetworks/gateways/connections/test/action|Teste une connexion de passerelle site à site.|
|/virtualNetworks/gateways/delete|Supprime la passerelle de réseau virtuel.|
|/virtualNetworks/gateways/downloadDeviceConfigurationScript/action|Télécharge le script de configuration d’appareil.|
|/virtualNetworks/gateways/downloadDiagnostics/action|Télécharge les diagnostics de la passerelle.|
|/virtualNetworks/gateways/listCircuitServiceKey/action|Récupère la clé de service du circuit.|
|/virtualNetworks/gateways/listPackage/action|Répertorie le package de passerelle de réseau virtuel.|
|/virtualNetworks/gateways/operationStatuses/read|Lit l’état de l’opération pour les passerelles de réseaux virtuels.|
|/virtualNetworks/gateways/packages/read|Obtient le package de passerelle de réseau virtuel.|
|/virtualNetworks/gateways/read|Obtient les passerelles de réseau virtuel.|
|/virtualNetworks/gateways/startDiagnostics/action|Démarre le diagnostic pour la passerelle de réseau virtuel.|
|/virtualNetworks/gateways/stopDiagnostics/action|Arrête le diagnostic pour la passerelle de réseau virtuel.|
|/virtualNetworks/gateways/write|Ajoute une passerelle de réseau virtuel.|
|/virtualNetworks/join/action|Joint le réseau virtuel.|
|/virtualNetworks/operationStatuses/read|Lit l’état de l’opération pour les réseaux virtuels.|
|/virtualNetworks/peer/action|Appaire un réseau virtuel avec un autre réseau virtuel.|
|/virtualNetworks/read|Obtenez le réseau virtuel.|
|/virtualNetworks/subnets/associatedNetworkSecurityGroups/delete|Supprime le groupe de sécurité réseau associé au sous-réseau.|
|/virtualNetworks/subnets/associatedNetworkSecurityGroups/operationStatuses/read|Lit l’état de l’opération pour le sous-réseau de réseau virtuel associé au groupe de sécurité réseau.|
|/virtualNetworks/subnets/associatedNetworkSecurityGroups/read|Obtient le groupe de sécurité réseau associé au sous-réseau.|
|/virtualNetworks/subnets/associatedNetworkSecurityGroups/write|Ajoute un groupe de sécurité réseau associé au sous-réseau.|
|/virtualNetworks/write|Ajoutez un nouveau réseau virtuel.|

## <a name="microsoftclassicstorage"></a>Microsoft.ClassicStorage

| Opération | Description |
|---|---|
|/capabilities/read|Affiche les fonctionnalités|
|/checkStorageAccountAvailability/action|Vérifie la disponibilité d’un compte de stockage.|
|/disks/read|Retourne le disque du compte de stockage.|
|/images/read|Retourne l’image.|
|/osImages/read|Retourne l’image du système d’exploitation.|
|/publicImages/read|Obtient l’image de machine virtuelle publique.|
|/quotas/read|Obtient le quota de l’abonnement.|
|/register/action|S’inscrire à un stockage classique|
|/storageAccounts/delete|Supprime le compte de stockage.|
|/storageAccounts/disks/delete|Supprime un disque de compte de stockage spécifique.|
|/storageAccounts/disks/operationStatuses/read|Lit l’état de l’opération pour la ressource.|
|/storageAccounts/disks/read|Retourne le disque du compte de stockage.|
|/storageAccounts/disks/write|Ajoute un disque de compte de stockage.|
|/storageAccounts/images/delete|Supprime une image du compte de stockage spécifique.|
|/storageAccounts/images/read|Retourne l’image du compte de stockage.|
|/storageAccounts/listKeys/action|Répertorie les clés d’accès des comptes de stockage.|
|/storageAccounts/operationStatuses/read|Lit l’état de l’opération pour la ressource.|
|/storageAccounts/osImages/delete|Supprime une image du système d’exploitation de compte de stockage spécifique.|
|/storageAccounts/osImages/read|Retourne l’image du système d’exploitation de compte de stockage.|
|/storageAccounts/read|Retourne le compte de stockage avec le compte spécifique.|
|/storageAccounts/regenerateKey/action|Régénère les clés d’accès existantes du compte de stockage.|
|/storageAccounts/services/diagnosticSettings/read|Obtient les paramètres des diagnostics.|
|/storageAccounts/services/diagnosticSettings/write|Ajoutez ou modifiez des paramètres de diagnostics.|
|/storageAccounts/services/metricDefinitions/read|Obtient les définitions de mesures.|
|/storageAccounts/services/metrics/read|Obtient les mesures.|
|/storageAccounts/services/read|Obtient les services disponibles.|
|/storageAccounts/write|Ajoute un nouveau compte de stockage.|

## <a name="microsoftcognitiveservices"></a>Microsoft.CognitiveServices

| Opération | Description |
|---|---|
|/accounts/delete|Supprime les comptes d’API|
|/accounts/listKeys/action|Afficher la liste des clés|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/read|Obtient le paramètre de diagnostic pour la ressource|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/write|Crée ou met à jour le paramètre de diagnostic pour la ressource|
|/accounts/providers/Microsoft.Insights/metricDefinitions/read|Obtient les métriques disponibles pour Cognitive Services|
|/accounts/read|Lit les comptes d’API.|
|/accounts/regenerateKey/action|Régénérer la clé|
|/accounts/skus/read|Lit les références disponibles pour une ressource existante.|
|/accounts/usages/read|Obtenir l’utilisation du quota pour une ressource existante.|
|/accounts/write|Écrit les comptes d’API.|
|/locations/checkSkuAvailability/action|Lit les références (SKU) disponibles pour un abonnement|
|/Operations/read|Répertorie toutes les opérations disponibles|
|/register/action|Enregistre l’abonnement à Cognitive Services|
|/skus/read|Lit les références (SKU) disponibles pour Cognitive Services|

## <a name="microsoftcommerce"></a>Microsoft.Commerce

| Opération | Description |
|---|---|
|/RateCard/read|Retourne les données, les métadonnées de ressource/compteur et les taux d’offre de l’abonnement concerné.|
|/UsageAggregates/read|Récupère l’utilisation de Microsoft Azure par un abonnement. Le résultat contient des données d’utilisation, des informations sur l’abonnement et la ressource agrégées, sur un intervalle de temps donné.|

## <a name="microsoftcompute"></a>Microsoft.Compute

| Opération | Description |
|---|---|
|/availabilitySets/delete|Supprimer le groupe à haute disponibilité|
|/availabilitySets/read|Obtenir les propriétés d’un groupe à haute disponibilité|
|/availabilitySets/vmSizes/read|Répertorier les tailles disponibles pour la création ou la mise à jour d’une machine virtuelle dans un groupe à haute disponibilité|
|/availabilitySets/write|Créer ou mettre à jour un groupe à haute disponibilité|
|/disks/beginGetAccess/action|Obtenir l’URI SAP du disque pour l’accès aux objets blob|
|/disks/delete|Supprimer le disque|
|/disks/endGetAccess/action|Révoquer l’URI SAP du disque|
|/disks/read|Obtenir les propriétés d’un disque|
|/disks/write|Créer ou mettre à jour un disque|
|/images/delete|Supprimer l’image|
|/images/read|Obtenir les propriétés de l’image|
|/images/write|Créer ou mettre à jour une image|
|/locations/capsOperations/read|Obtient l’état d’une opération de plafonnement asynchrone|
|/locations/diskOperations/read|Obtient l’état d’une opération de disque asynchrone|
|/locations/operations/read|Afficher l’état d’une opération asynchrone|
|/locations/publishers/artifacttypes/offers/read|Obtient les propriétés d’une offre d’image de plateforme|
|/locations/publishers/artifacttypes/offers/skus/read|Obtient les propriétés d’une référence (SKU) d’image de plateforme|
|/locations/publishers/artifacttypes/offers/skus/versions/read|Obtient les propriétés d’une version d’image de plateforme|
|/locations/publishers/artifacttypes/types/read|Obtient les propriétés d’un type d’extension de machine virtuelle|
|/locations/publishers/artifacttypes/types/versions/read|Obtient les propriétés d’une version d’extension de machine virtuelle|
|/locations/publishers/read|Obtient les propriétés d’un éditeur|
|/locations/runCommands/read|Répertorie les commandes d’exécution disponibles dans un emplacement|
|/locations/usages/read|Afficher les limites du service et les quantités en cours d’utilisation pour les ressources de calcul de l’abonnement dans un emplacement|
|/locations/vmSizes/read|Répertorier les tailles de machines virtuelles disponibles dans un emplacement|
|/operations/read|Répertorier les opérations disponibles dans le fournisseur de ressources Microsoft.Compute|
|/register/action|Inscrit l’abonnement auprès du fournisseur de ressources Microsoft.Compute|
|/restorePointCollections/delete|Supprimer la collection de points de restauration et les points de restauration contenus|
|/restorePointCollections/read|Obtenir les propriétés d’une collection de points de restauration|
|/restorePointCollections/restorePoints/delete|Supprimer le point de restauration|
|/restorePointCollections/restorePoints/read|Obtenir les propriétés d’un point de restauration|
|/restorePointCollections/restorePoints/retrieveSasUris/action|Obtenir les propriétés d’un point de restauration, ainsi que les URI SAP des objets blob|
|/restorePointCollections/restorePoints/write|Créer un nouveau point de restauration|
|/restorePointCollections/write|Crée une nouvelle collection de points de restauration ou met à jour une collection existante|
|/sharedVMImages/delete|Supprime l’image de machine virtuelle partagée|
|/sharedVMImages/read|Obtient les propriétés d’une image de machine virtuelle partagée|
|/sharedVMImages/versions/delete|Supprime une version d’image de machine virtuelle partagée|
|/sharedVMImages/versions/read|Obtient les propriétés d’une version image de machine virtuelle partagée|
|/sharedVMImages/versions/replicate/action|Réplique une version d’image de machine virtuelle partagée dans des régions cibles|
|/sharedVMImages/versions/write|Crée ou met à jour une version d’image de machine virtuelle partagée|
|/sharedVMImages/write|Crée ou met à jour une image de machine virtuelle partagée|
|/skus/read|Obtient la liste des références (SKU) Microsoft.Compute disponibles pour votre abonnement|
|/snapshots/beginGetAccess/action|Obtient l’URI SAP de la capture instantanée pour l’accès aux objets blob|
|/snapshots/delete|Supprimer une capture instantanée|
|/snapshots/endGetAccess/action|Révoque l’URI SAP de la capture instantanée|
|/snapshots/read|Obtenir les propriétés d’une capture instantanée|
|/snapshots/write|Créer ou mettre à jour une capture instantanée|
|/virtualMachines/capture/action|Capturer la machine virtuelle en copiant les disques durs virtuels et générer un modèle qui peut être utilisé pour créer des machines virtuelles similaires|
|/virtualMachines/convertToManagedDisks/action|Convertir les disques basés sur des objets blob de la machine virtuelle en disques gérés|
|/virtualMachines/deallocate/action|Mettre hors tension la machine virtuelle et libérer les ressources de calcul|
|/virtualMachines/delete|Supprimer la machine virtuelle|
|/virtualMachines/extensions/delete|Supprimer l’extension de machine virtuelle|
|/virtualMachines/extensions/read|Afficher les propriétés d’une extension de machine virtuelle|
|/virtualMachines/extensions/write|Créer ou mettre à jour une extension de machine virtuelle|
|/virtualMachines/generalize/action|Définir l’état de la machine virtuelle sur Généralisée et préparer la machine virtuelle pour la capture|
|/virtualMachines/instanceView/read|Afficher l’état d’exécution détaillé de la machine virtuelle et de ses ressources|
|/virtualMachines/performMaintenance/action|Performs Maintenance Operation on the VM.|
|/virtualMachines/powerOff/action|Mettre hors tension la machine virtuelle. Notez que la machine virtuelle sera toujours facturée.|
|/virtualMachines/providers/Microsoft.Insights/metricDefinitions/read|Lit les définitions de métrique de machine virtuelle|
|/virtualMachines/read|Obtenir les propriétés d’une machine virtuelle|
|/virtualMachines/redeploy/action|Redéployer la machine virtuelle|
|/virtualMachines/reimage/action|Réimage une machine virtuelle utilisant un disque de différenciation|
|/virtualMachines/restart/action|Redémarrer la machine virtuelle|
|/virtualMachines/runCommand/action|Exécute un script prédéfini sur la machine virtuelle|
|/virtualMachines/start/action|Démarrer la machine virtuelle|
|/virtualMachines/vmSizes/read|Répertorier les tailles disponibles pour la mise à jour de la machine virtuelle|
|/virtualMachines/write|Créer ou mettre à jour une machine virtuelle|
|/virtualMachineScaleSets/deallocate/action|Met hors tension et libère les ressources de calcul pour les instances du groupe de machines virtuelles identiques |
|/virtualMachineScaleSets/delete|Supprime le groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/delete/action|Supprime les instances du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/extensions/delete|Supprime l’extension de groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/extensions/read|Obtient les propriétés d’une extension de groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/extensions/write|Crée ou met à jour une extension de groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/forceRecoveryServiceFabricPlatformUpdateDomainWalk/action|Nécessite de parcourir manuellement les domaines de mise à jour de plateforme d’un groupe de machines virtuelles identiques Service Fabric pour achever une mise à jour en attente bloquée|
|/virtualMachineScaleSets/instanceView/read|Obtient la vue d’instance du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/manualUpgrade/action|Nécessite de mettre à jour manuellement les instances avec le dernier modèle du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/networkInterfaces/read|Obtient les propriétés de toutes les interfaces réseau d’un groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/osUpgradeHistory/read|Obtient l’historique des mises à niveau du système d’exploitation pour un groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/performMaintenance/action|Effectue une maintenance planifiée sur les instances du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/powerOff/action|Met hors tension les instances du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/providers/Microsoft.Insights/metricDefinitions/read|Lit les définitions de métrique du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/publicIPAddresses/read|Obtient les propriétés de toutes les adresses IP publiques d’un groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/read|Obtient les propriétés d’un groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/redeploy/action|Redéploie les instances du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/reimage/action|Réimage les instances du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/restart/action|Redémarre les instances du groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/rollingUpgrades/cancel/action|Annule la mise à niveau propagée d’un groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/rollingUpgrades/read|Obtient l’état de la dernière mise à niveau propagée d’un groupe de machines virtuelles identiques|
|/virtualMachineScaleSets/scale/action|Vérifie si un groupe de machines virtuelles identiques existant peut être mis à l’échelle vers un nombre d’instances spécifié|
|/virtualMachineScaleSets/skus/read|Lists the valid SKUs for an existing Virtual Machine Scale Set|
|/virtualMachineScaleSets/start/action|Starts the instances of the Virtual Machine Scale Set|
|/virtualMachineScaleSets/virtualMachines/deallocate/action|Powers off and releases the compute resources for a Virtual Machine in a VM Scale Set.|
|/virtualMachineScaleSets/virtualMachines/delete|Delete a specific Virtual Machine in a VM Scale Set.|
|/virtualMachineScaleSets/virtualMachines/instanceView/read|Retrieves the instance view of a Virtual Machine in a VM Scale Set.|
|/virtualMachineScaleSets/virtualMachines/networkInterfaces/ ipConfigurations/publicIPAddresses/read|Get properties of public IP address created using Virtual Machine Scale Set. Virtual Machine Scale Set can create at most one public IP per ipconfiguration (private IP)|
|/virtualMachineScaleSets/virtualMachines/networkInterfaces/ipConfigurations/read|Get properties of one or all IP configurations of a network interface created using Virtual Machine Scale Set. IP configurations represent private IPs|
|/virtualMachineScaleSets/virtualMachines/networkInterfaces/read|Get properties of one or all network interfaces of a virtual machine created using Virtual Machine Scale Set|
|/virtualMachineScaleSets/virtualMachines/performMaintenance/action|Performs planned maintenance on a Virtual Machine instance in a Virtual Machine Scale Set|
|/virtualMachineScaleSets/virtualMachines/powerOff/action|Powers Off a Virtual Machine instance in a VM Scale Set.|
|/virtualMachineScaleSets/virtualMachines/providers/ Microsoft.Insights/metricDefinitions/read|Reads Virtual Machine in Scale Set Metric Definitions|
|/virtualMachineScaleSets/virtualMachines/read|Retrieves the properties of a Virtual Machine in a VM Scale Set|
|/virtualMachineScaleSets/virtualMachines/redeploy/action|Redeploys a Virtual Machine instance in a Virtual Machine Scale Set|
|/virtualMachineScaleSets/virtualMachines/reimage/action|Reimages a Virtual Machine instance in a Virtual Machine Scale Set.|
|/virtualMachineScaleSets/virtualMachines/restart/action|Restarts a Virtual Machine instance in a VM Scale Set.|
|/virtualMachineScaleSets/virtualMachines/start/action|Starts a Virtual Machine instance in a VM Scale Set.|
|/virtualMachineScaleSets/virtualMachines/write|Updates the properties of a Virtual Machine in a VM Scale Set|
|/virtualMachineScaleSets/write|Creates a new Virtual Machine Scale Set or updates an existing one|

## <a name="microsoftconsumption"></a>Microsoft.Consumption

| Operation | Description |
|---|---|
|/balances/read|List the utilization summary for a billing period for a management group.|
|/budgets/read|List the budgets by a subscription or a management group.|
|/budgets/write|Creates, update and delete the budgets by a subscription or a management group.|
|/marketplaces/read|List the marketplace resource usage details for a scope for EA and WebDirect subscriptions.|
|/operations/read|List all supported operations by Microsoft.Consumption resource provider.|
|/pricesheets/read|List the Pricesheets data for a subscription or a management group.|
|/reservationDetails/read|List the utilization details for reserved instances by reservation order or managment groups. The details data is per instance per day level.|
|/reservationSummaries/read|List the utilization summary for reserved instances by reservation order or managment groups. The summary data is either at monthly or daily level.|
|/reservationTransactions/read|List the transaction history for reserved instances by management groups.|
|/terms/read|List the terms for a subscription or a management group.|
|/usageDetails/read|List the usage details for a scope for EA and WebDirect subscriptions.|

## <a name="microsoftcontainerinstance"></a>Microsoft.ContainerInstance

| Operation | Description |
|---|---|
|/containerGroups/containers/logs/read|Get logs for a specific container.|
|/containerGroups/delete|Delete the specific container group.|
|/containerGroups/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the container group.|
|/containerGroups/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the container group.|
|/containerGroups/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for container group.|
|/containerGroups/read|Get all container goups.|
|/containerGroups/write|Create or update a specific container group.|

## <a name="microsoftcontainerregistry"></a>Microsoft.ContainerRegistry

| Operation | Description |
|---|---|
|/checkNameAvailability/read|Checks whether the container registry name is available for use.|
|/locations/operationResults/read|Gets an async operation result|
|/operations/read|Lists all of the available Azure Container Registry REST API operations|
|/register/action|Registers the subscription for the container registry resource provider and enables the creation of container registries.|
|/registries/delete|Deletes a container registry.|
|/registries/eventGridFilters/delete|Deletes an event grid filter from a container registry.|
|/registries/eventGridFilters/read|Gets the properties of the specified event grid filter or lists all the event grid filters for the specified container registry.|
|/registries/eventGridFilters/write|Creates or updates an event grid filter for a container registry with the specified parameters.|
|/registries/listCredentials/action|Lists the login credentials for the specified container registry.|
|/registries/listUsages/read|Lists the quota usages for the specified container registry.|
|/registries/operationStatuses/read|Gets a registry async operation status|
|/registries/read|Gets the properties of the specified container registry or lists all the container registries under the specified resource group or subscription.|
|/registries/regenerateCredential/action|Regenerates one of the login credentials for the specified container registry.|
|/registries/replications/delete|Deletes a replication from a container registry.|
|/registries/replications/operationStatuses/read|Gets a replication async operation status|
|/registries/replications/read|Gets the properties of the specified replication or lists all the replications for the specified container registry.|
|/registries/replications/write|Creates or updates a replication for a container registry with the specified parameters.|
|/registries/webhooks/delete|Deletes a webhook from a container registry.|
|/registries/webhooks/getCallbackConfig/action|Gets the configuration of service URI and custom headers for the webhook.|
|/registries/webhooks/listEvents/action|Lists recent events for the specified webhook.|
|/registries/webhooks/operationStatuses/read|Gets a webhook async operation status|
|/registries/webhooks/ping/action|Triggers a ping event to be sent to the webhook.|
|/registries/webhooks/read|Gets the properties of the specified webhook or lists all the webhooks for the specified container registry.|
|/registries/webhooks/write|Creates or updates a webhook for a container registry with the specified parameters.|
|/registries/write|Creates or updates a container registry with the specified parameters.|

## <a name="microsoftcontainerservice"></a>Microsoft.ContainerService

| Operation | Description |
|---|---|
|/containerServices/delete|Deletes the specified Container Service|
|/containerServices/read|Gets the specified Container Service|
|/containerServices/write|Puts or Updates the specified Container Service|

## <a name="microsoftcontentmoderator"></a>Microsoft.ContentModerator

| Operation | Description |
|---|---|
|/applications/delete|Delete Operation|
|/applications/listSecrets/action|List Secrets|
|/applications/listSingleSignOnToken/action|Read Single Sign On Tokens|
|/applications/read|Read Operation|
|/applications/write|Write Operation|
|/applications/write|Write Operation|
|/listCommunicationPreference/action|List communication preference|
|/operations/read|read operations|
|/updateCommunicationPreference/action|Update communication preference|

## <a name="microsoftcustomerinsights"></a>Microsoft.CustomerInsights

| Operation | Description |
|---|---|
|/hubs/adobemetadata/action|Create or Update any Azure Customer Insights Adobe Metadata|
|/hubs/adobemetadata/read|Read any Azure Customer Insights Adobe Metadata|
|/hubs/authorizationPolicies/delete|Delete any Azure Customer Insights Shared Access Signature Policy|
|/hubs/authorizationPolicies/read|Read any Azure Customer Insights Shared Access Signature Policy|
|/hubs/authorizationPolicies/regeneratePrimaryKey/action|Regenerate Azure Customer Insights Shared Access Signature Policy primary key|
|/hubs/authorizationPolicies/regenerateSecondaryKey/action|Regenerate Azure Customer Insights Shared Access Signature Policy secondary key|
|/hubs/authorizationPolicies/write|Create or Update any Azure Customer Insights Shared Access Signature Policy|
|/hubs/connectors/activate/action|Activate any Azure Customer Insights Connector|
|/hubs/connectors/activate/action|Activate any Azure Customer Insights Connector|
|/hubs/connectors/delete|Delete any Azure Customer Insights Connector|
|/hubs/connectors/getruntimestatus/action|Get any Azure Customer Insights Connector runtime status|
|/hubs/connectors/mappings/activate/action|Activate any Azure Customer Insights Connector Mapping|
|/hubs/connectors/mappings/delete|Delete any Azure Customer Insights Connector Mapping|
|/hubs/connectors/mappings/operations/read|Read any Azure Customer Insights Connector Mapping operation result|
|/hubs/connectors/mappings/read|Read any Azure Customer Insights Connector Mapping|
|/hubs/connectors/mappings/write|Create or Update any Azure Customer Insights Connector Mapping|
|/hubs/connectors/operations/read|Read any Azure Customer Insights Connector operation result|
|/hubs/connectors/read|Read any Azure Customer Insights Connector|
|/hubs/connectors/saveauthinfo/action|Create or Update any Azure Customer Insights Connector Authentication Infomation|
|/hubs/connectors/update/action|Update any Azure Customer Insights Connector|
|/hubs/connectors/write|Create or Update any Azure Customer Insights Connector|
|/hubs/crmmetadata/action|Create or Update any Azure Customer Insights Crm Metadata|
|/hubs/crmmetadata/read|Read any Azure Customer Insights Crm Metadata|
|/hubs/delete|Delete any Azure Customer Insights Hub|
|/hubs/gdpr/delete|Delete any Azure Customer Insights Gdpr|
|/hubs/gdpr/read|Read any Azure Customer Insights Gdpr|
|/hubs/gdpr/write|Create or Update any Azure Customer Insights Gdpr|
|/hubs/getbillingcredits/read|Get Azure Customer Insights Hub Billing Credits|
|/hubs/getbillinghistory/read|Get Azure Customer Insights Hub Billing History|
|/hubs/images/delete|Delete any Azure Customer Insights Image|
|/hubs/images/read|Read any Azure Customer Insights Image|
|/hubs/images/write|Create or Update any Azure Customer Insights Image|
|/hubs/interactions/delete|Delete any azure Customer Insights Interactions|
|/hubs/interactions/operations/read|Read any Azure Customer Insights Interaction operation result|
|/hubs/interactions/read|Read any Azure Customer Insights Interaction|
|/hubs/interactions/suggestrelationshiplinks/action|Suggest RelationShip Links for any Azure Customer Insights Interactions|
|/hubs/interactions/write|Create or Update any Azure Customer Insights Interaction|
|/hubs/kpi/delete|Delete any Azure Customer Insights Key Performance Indicator|
|/hubs/kpi/operations/read|Read any Azure Customer Insights Key Performance Indicators operation result|
|/hubs/kpi/read|Read any Azure Customer Insights Key Performance Indicator|
|/hubs/kpi/reprocess/action|Reprocess any Azure Customer Insights Key Performance Indicators|
|/hubs/kpi/write|Create or Update any Azure Customer Insights Key Performance Indicator|
|/hubs/links/delete|Delete any Azure Customer Insights Links|
|/hubs/links/operations/read|Read any Azure Customer Insights Links operation result|
|/hubs/links/read|Read any Azure Customer Insights Links|
|/hubs/links/write|Create or Update any Azure Customer Links|
|/hubs/msemetadata/action|Create or Update any Azure Customer Insights Mse Metadata|
|/hubs/msemetadata/read|Read any Azure Customer Insights Mse Metadata|
|/hubs/operationresults/read|Get Azure Customer Insights Hub Operation Results|
|/hubs/predictions/delete|Delete any Azure Customer Insights Predictions|
|/hubs/predictions/operations/read|Read any Azure Customer Insights Predictions operation result|
|/hubs/predictions/read|Read any Azure Customer Insights Predictions|
|/hubs/predictions/write|Create or Update any Azure Customer Predictions|
|/hubs/predictivematchpolicies/delete|Delete any Azure Customer Insights Predictive Match Policies|
|/hubs/predictivematchpolicies/operations/read|Read any Azure Customer Insights Predictive Match Policies operation result|
|/hubs/predictivematchpolicies/read|Read any Azure Customer Insights Predictive Match Policies|
|/hubs/predictivematchpolicies/write|Create or Update any Azure Customer Insights Predictive Match Policies|
|/hubs/profiles/delete|Delete any Azure Customer Insights Profile|
|/hubs/profiles/operations/read|Read any Azure Customer Insights Profile operation result|
|/hubs/profiles/read|Read any Azure Customer Insights Profile|
|/hubs/profiles/write|Write any Azure Customer Insights Profile|
|/hubs/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/hubs/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/hubs/providers/Microsoft.Insights/logDefinitions/read|Gets the available logs for resource|
|/hubs/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for resource|
|/hubs/read|Read any Azure Customer Insights Hub|
|/hubs/relationshiplinks/delete|Delete any Azure Customer Insights Relationship Links|
|/hubs/relationshiplinks/operations/read|Read any Azure Customer Insights Relationship Links operation result|
|/hubs/relationshiplinks/read|Read any Azure Customer Insights Relationship Links|
|/hubs/relationshiplinks/write|Create or Update any Azure Customer Insights Relationship Links|
|/hubs/relationships/delete|Delete any Azure Customer Insights Relationships|
|/hubs/relationships/operations/read|Read any Azure Customer Insights Relationships operation result|
|/hubs/relationships/read|Read any Azure Customer Insights Relationships|
|/hubs/relationships/write|Create or Update any Azure Customer Insights Relationships|
|/hubs/roleAssignments/delete|Delete any Azure Customer Insights Rbac Assignment|
|/hubs/roleAssignments/operations/read|Read any Azure Customer Insights Rbac Assignment operation result|
|/hubs/roleAssignments/read|Read any Azure Customer Insights Rbac Assignment|
|/hubs/roleAssignments/write|Create or Update any Azure Customer Insights Rbac Assignment|
|/hubs/roles/read|Read any Azure Customer Insights Rbac Roles|
|/hubs/salesforcemetadata/action|Create or Update any Azure Customer Insights SalesForce Metadata|
|/hubs/salesforcemetadata/read|Read any Azure Customer Insights SalesForce Metadata|
|/hubs/segments/delete|Delete any Azure Customer Insights Segments|
|/hubs/segments/dynamic/action|Management any Azure Customer Insight Dynamic Segments|
|/hubs/segments/read|Read any Azure Customer Insights Segments|
|/hubs/segments/static/action|Management any Azure Customer Insight Static Segments|
|/hubs/segments/write|Create or Update any Azure Customer Insights Segments|
|/hubs/sqlconnectionstrings/delete|Delete any Azure Customer Insights SqlConnectionStrings|
|/hubs/sqlconnectionstrings/read|Read any Azure Customer Insights SqlConnectionStrings|
|/hubs/sqlconnectionstrings/write|Create or Update any Azure Customer Insights SqlConnectionStrings|
|/hubs/suggesttypeschema/action|Generate Suggest Type Schema from sample data|
|/hubs/tenantmanagement/read|Manage any Azure Customer Insights hub settings|
|/hubs/views/delete|Delete any Azure Customer Insights App View|
|/hubs/views/read|Read any Azure Customer Insights App View|
|/hubs/views/write|Create or Update any Azure Customer Insights App View|
|/hubs/widgettypes/read|Read any Azure Customer Insights App Widget Types|
|/hubs/write|Create or Update any Azure Customer Insights Hub|
|/operations/read|Read Azure Customer Insights Api Metadatas|
|/register/action|Registers the subscription for the Customer Insights resource provider and enables the creation of Customer Insights resources|
|/unregister/action|Unregisters the subscription for the Customer Insights resource provider|

## <a name="microsoftdatacatalog"></a>Microsoft.DataCatalog

| Operation | Description |
|---|---|
|/catalogs/delete|Deletes the catalog.|
|/catalogs/read|Get properties for catalog or catalogs under subscription or resource group.|
|/catalogs/write|Creates catalog or updates the tags and properties for the catalog.|
|/checkNameAvailability/action|Checks catalog name availability for tenant.|
|/operations/read|Lists operations available on Microsoft.DataCatalog resource provider.|
|/register/action|Registers subscription with Microsoft.DataCatalog resource provider.|
|/unregister/action|Unregisters subscription from Microsoft.DataCatalog resource provider.|

## <a name="microsoftdatafactory"></a>Microsoft.DataFactory

| Operation | Description |
|---|---|
|/datafactories/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/datafactories/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/datafactories/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for datafactories|
|/factories/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/factories/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/factories/providers/Microsoft.Insights/logDefinitions/read|Gets the available logs for factories|
|/factories/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for factories|

## <a name="microsoftdatalakeanalytics"></a>Microsoft.DataLakeAnalytics

| Operation | Description |
|---|---|
|/accounts/computePolicies/delete|Delete a compute policy.|
|/accounts/computePolicies/read|Get information about a compute policy.|
|/accounts/computePolicies/write|Create or update a compute policy.|
|/accounts/dataLakeStoreAccounts/delete|Unlink a DataLakeStore account from a DataLakeAnalytics account.|
|/accounts/dataLakeStoreAccounts/read|Get information about a linked DataLakeStore account of a DataLakeAnalytics account.|
|/accounts/dataLakeStoreAccounts/write|Create or update a linked DataLakeStore account of a DataLakeAnalytics account.|
|/accounts/delete|Delete a DataLakeAnalytics account.|
|/accounts/firewallRules/delete|Delete a firewall rule.|
|/accounts/firewallRules/read|Get information about a firewall rule.|
|/accounts/firewallRules/write|Create or update a firewall rule.|
|/accounts/operationResults/read|Get result of a DataLakeAnalytics account operation.|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/read|Get the diagnostic settings for the DataLakeAnalytics account.|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/write|Create or update the diagnostic settings for the DataLakeAnalytics account.|
|/accounts/providers/Microsoft.Insights/logDefinitions/read|Get the available logs for the DataLakeAnalytics account.|
|/accounts/providers/Microsoft.Insights/metricDefinitions/read|Get the available metrics for the DataLakeAnalytics account.|
|/accounts/read|Get information about an existing DataLakeAnalytics account.|
|/accounts/storageAccounts/Containers/listSasTokens/action|List SAS tokens for storage containers of a linked Storage account of a DataLakeAnalytics account.|
|/accounts/storageAccounts/Containers/read|Get containers of a linked Storage account of a DataLakeAnalytics account.|
|/accounts/storageAccounts/delete|Unlink a Storage account from a DataLakeAnalytics account.|
|/accounts/storageAccounts/read|Get information about a linked Storage account of a DataLakeAnalytics account.|
|/accounts/storageAccounts/write|Create or update a linked Storage account of a DataLakeAnalytics account.|
|/accounts/TakeOwnership/action|Grant permissions to cancel jobs submitted by other users.|
|/accounts/write|Create or update a DataLakeAnalytics account.|
|/locations/capability/read|Get capability information of a subscription regarding using DataLakeAnalytics.|
|/locations/checkNameAvailability/action|Check availability of a DataLakeAnalytics account name.|
|/locations/operationResults/read|Get result of a DataLakeAnalytics account operation.|
|/operations/read|Get available operations of DataLakeAnalytics.|
|/register/action|Register subscription to DataLakeAnalytics.|

## <a name="microsoftdatalakestore"></a>Microsoft.DataLakeStore

| Operation | Description |
|---|---|
|/accounts/delete|Delete a DataLakeStore account.|
|/accounts/enableKeyVault/action|Enable KeyVault for a DataLakeStore account.|
|/accounts/firewallRules/delete|Delete a firewall rule.|
|/accounts/firewallRules/read|Get information about a firewall rule.|
|/accounts/firewallRules/write|Create or update a firewall rule.|
|/accounts/operationResults/read|Get result of a DataLakeStore account operation.|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/read|Get the diagnostic settings for the DataLakeStore account.|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/write|Create or update the diagnostic settings for the DataLakeStore account.|
|/accounts/providers/Microsoft.Insights/logDefinitions/read|Get the available logs for the DataLakeStore account.|
|/accounts/providers/Microsoft.Insights/metricDefinitions/read|Get the available metrics for the DataLakeStore account.|
|/accounts/read|Get information about an existing DataLakeStore account.|
|/accounts/Superuser/action|Grant Superuser on Data Lake Store when granted with Microsoft.Authorization/roleAssignments/write.|
|/accounts/trustedIdProviders/delete|Delete a trusted identity provider.|
|/accounts/trustedIdProviders/read|Get information about a trusted identity provider.|
|/accounts/trustedIdProviders/write|Create or update a trusted identity provider.|
|/accounts/write|Create or update a DataLakeStore account.|
|/locations/capability/read|Get capability information of a subscription regarding using DataLakeStore.|
|/locations/checkNameAvailability/action|Check availability of a DataLakeStore account name.|
|/locations/operationResults/read|Get result of a DataLakeStore account operation.|
|/operations/read|Get available operations of DataLakeStore.|
|/register/action|Register subscription to DataLakeStore.|

## <a name="microsoftdbformysql"></a>Microsoft.DBforMySQL

| Operation | Description |
|---|---|
|/locations/performanceTiers/read|Returns the list of Performance Tiers available.|
|/performanceTiers/read|Returns the list of Performance Tiers available.|
|/servers/delete|Deletes an existing server.|
|/servers/firewallRules/delete|Deletes an existing firewall rule.|
|/servers/firewallRules/read|Return the list of firewall rules for a server or gets the properties for the specified firewall rule.|
|/servers/firewallRules/write|Creates a firewall rule with the specified parameters or update an existing rule.|
|/servers/providers/Microsoft.Insights/diagnosticSettings/read|Gets the disagnostic setting for the resource|
|/servers/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/servers/providers/Microsoft.Insights/metricDefinitions/read|Return types of metrics that are available for databases|
|/servers/read|Return the list of servers or gets the properties for the specified server.|
|/servers/recoverableServers/read|Return the recoverable MySQL Server info|
|/servers/virtualNetworkRules/delete|Deletes an existing Virtual Network Rule|
|/servers/virtualNetworkRules/read|Return the list of virtual network rules or gets the properties for the specified virtual network rule.|
|/servers/virtualNetworkRules/write|Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule.|
|/servers/write|Creates a server with the specified parameters or update the properties or tags for the specified server.|

## <a name="microsoftdbforpostgresql"></a>Microsoft.DBforPostgreSQL

| Operation | Description |
|---|---|
|/locations/performanceTiers/read|Returns the list of Performance Tiers available.|
|/performanceTiers/read|Returns the list of Performance Tiers available.|
|/servers/delete|Deletes an existing server.|
|/servers/firewallRules/delete|Deletes an existing firewall rule.|
|/servers/firewallRules/read|Return the list of firewall rules for a server or gets the properties for the specified firewall rule.|
|/servers/firewallRules/write|Creates a firewall rule with the specified parameters or update an existing rule.|
|/servers/providers/Microsoft.Insights/diagnosticSettings/read|Gets the disagnostic setting for the resource|
|/servers/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/servers/providers/Microsoft.Insights/logDefinitions/read|Return types of logs that are available for databases|
|/servers/providers/Microsoft.Insights/metricDefinitions/read|Return types of metrics that are available for databases|
|/servers/read|Return the list of servers or gets the properties for the specified server.|
|/servers/recoverableServers/read|Return the recoverable PostgreSQL Server info|
|/servers/virtualNetworkRules/delete|Deletes an existing Virtual Network Rule|
|/servers/virtualNetworkRules/read|Return the list of virtual network rules or gets the properties for the specified virtual network rule.|
|/servers/virtualNetworkRules/write|Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule.|
|/servers/write|Creates a server with the specified parameters or update the properties or tags for the specified server.|

## <a name="microsoftdevices"></a>Microsoft.Devices

| Operation | Description |
|---|---|
|/checkNameAvailability/Action|Check If IotHub name is available|
|/checkProvisioningServiceNameAvailability/Action|Check If IotHub name is available|
|/ElasticPools/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/ElasticPools/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/elasticPools/iotHubTenants/Delete|Delete the IotHub tenant resource|
|/ElasticPools/IotHubTenants/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/ElasticPools/IotHubTenants/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/elasticPools/iotHubTenants/eventHubEndpoints/consumerGroups/Delete|Delete EventHub Consumer Group|
|/elasticPools/iotHubTenants/eventHubEndpoints/consumerGroups/Read|Get EventHub Consumer Group(s)|
|/elasticPools/iotHubTenants/eventHubEndpoints/consumerGroups/Write|Create EventHub Consumer Group|
|/elasticPools/iotHubTenants/exportDevices/Action|Export Devices|
|/elasticPools/iotHubTenants/getStats/Read|Gets the IotHub tenant stats resource|
|/elasticPools/iotHubTenants/importDevices/Action|Import Devices|
|/elasticPools/iotHubTenants/iotHubKeys/listkeys/Action|Gets the IotHub tenant key|
|/elasticPools/iotHubTenants/jobs/Read|Get Job(s) details submitted on given IotHub|
|/elasticPools/iotHubTenants/listKeys/Action|Gets IotHub tenant keys|
|/ElasticPools/IotHubTenants/logDefinitions/read|Gets the available log definitions for the IotHub Service|
|/ElasticPools/IotHubTenants/metricDefinitions/read|Gets the available metrics for the IotHub service|
|/elasticPools/iotHubTenants/quotaMetrics/Read|Get Quota Metrics|
|/elasticPools/iotHubTenants/Read|Gets the IotHub tenant resource|
|/elasticPools/iotHubTenants/routing/routes/$testall/Action|Test a message against all existing Routes|
|/elasticPools/iotHubTenants/routing/routes/$testnew/Action|Test a message against a provided test Route|
|/elasticPools/iotHubTenants/routingEndpointsHealth/Read|Gets the health of all routing Endpoints for an IotHub|
|/elasticPools/iotHubTenants/Write|Create or Update the IotHub tenant resource|
|/ElasticPools/metricDefinitions/read|Gets the available metrics for the IotHub service|
|/iotHubs/certificates/generateVerificationCode/Action|Generate Verification code|
|/iotHubs/certificates/verify/Action|Verify Certificate resource|
|/iotHubs/Delete|Delete IotHub Resource|
|/IotHubs/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/IotHubs/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/iotHubs/eventGridFilters/Delete|Deletes the Event Grid filter|
|/iotHubs/eventGridFilters/Read|Gets the Event Grid filter|
|/iotHubs/eventGridFilters/Write|Create new or Update existing Event Grid filter|
|/iotHubs/eventHubEndpoints/consumerGroups/Delete|Delete EventHub Consumer Group|
|/iotHubs/eventHubEndpoints/consumerGroups/Read|Get EventHub Consumer Group(s)|
|/iotHubs/eventHubEndpoints/consumerGroups/Write|Create EventHub Consumer Group|
|/iotHubs/exportDevices/Action|Export Devices|
|/iotHubs/importDevices/Action|Import Devices|
|/iotHubs/iotHubKeys/listkeys/Action|Get IotHub Key for the given name|
|/iotHubs/iotHubStats/Read|Get IotHub Statistics|
|/iotHubs/jobs/Read|Get Job(s) details submitted on given IotHub|
|/iotHubs/listkeys/Action|Get all IotHub Keys|
|/IotHubs/logDefinitions/read|Gets the available log definitions for the IotHub Service|
|/IotHubs/metricDefinitions/read|Gets the available metrics for the IotHub service|
|/iotHubs/quotaMetrics/Read|Get Quota Metrics|
|/iotHubs/Read|Gets the IotHub resource(s)|
|/iotHubs/routing/$testall/Action|Test a message against all existing Routes|
|/iotHubs/routing/$testnew/Action|Test a message against a provided test Route|
|/iotHubs/routingEndpointsHealth/Read|Gets the health of all routing Endpoints for an IotHub|
|/iotHubs/skus/Read|Get valid IotHub Skus|
|/iotHubs/Write|Create or update IotHub Resource|
|/operations/Read|Get All ResourceProvider Operations|
|/provisioningServices/certificates/generateVerificationCode/Action|Generate Verification code|
|/provisioningServices/certificates/verify/Action|Verify Certificate resource|
|/provisioningServices/Delete|Delete IotDps resource|
|/provisioningServices/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/provisioningServices/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/provisioningServices/listkeys/Action|Get all IotDps keys|
|/provisioningServices/logDefinitions/read|Gets the available log definitions for the provisioning Service|
|/provisioningServices/metricDefinitions/read|Gets the available metrics for the provisioning service|
|/provisioningServices/ProvisioningServiceKeys/listkeys/Action|Get IotDps Keys for key name|
|/provisioningServices/Read|Get IotDps resource|
|/provisioningServices/skus/Read|Get valid IotDps Skus|
|/provisioningServices/Write|Create IotDps resource|
|/register/action|Register the subscription for the IotHub resource provider and enables the creation of IotHub resources|
|/register/action|Register the subscription for the IotHub resource provider and enables the creation of IotHub resources|
|/usages/Read|Get subscription usage details for this provider.|

## <a name="microsoftdevtestlab"></a>Microsoft.DevTestLab

| Operation | Description |
|---|---|
|/labCenters/delete|Delete lab centers.|
|/labCenters/read|Read lab centers.|
|/labCenters/write|Add or modify lab centers.|
|/labs/artifactSources/armTemplates/read|Read azure resource manager templates.|
|/labs/artifactSources/artifacts/GenerateArmTemplate/action|Generates an ARM template for the given artifact, uploads the required files to a storage account, and validates the generated artifact.|
|/labs/artifactSources/artifacts/read|Read artifacts.|
|/labs/artifactSources/delete|Delete artifact sources.|
|/labs/artifactSources/read|Read artifact sources.|
|/labs/artifactSources/write|Add or modify artifact sources.|
|/labs/ClaimAnyVm/action|Claim a random claimable virtual machine in the lab.|
|/labs/costs/read|Read costs.|
|/labs/costs/write|Add or modify costs.|
|/labs/CreateEnvironment/action|Create virtual machines in a lab.|
|/labs/customImages/delete|Delete custom images.|
|/labs/customImages/read|Read custom images.|
|/labs/customImages/write|Add or modify custom images.|
|/labs/delete|Delete labs.|
|/labs/ExportResourceUsage/action|Exports the lab resource usage into a storage account|
|/labs/formulas/delete|Delete formulas.|
|/labs/formulas/read|Read formulas.|
|/labs/formulas/write|Add or modify formulas.|
|/labs/galleryImages/read|Read gallery images.|
|/labs/GenerateUploadUri/action|Generate a URI for uploading custom disk images to a Lab.|
|/labs/ImportVirtualMachine/action|Import a virtual machine into a different lab.|
|/labs/ListVhds/action|List disk images available for custom image creation.|
|/labs/notificationChannels/delete|Delete notificationchannels.|
|/labs/notificationChannels/Notify/action|Send notification to provided channel.|
|/labs/notificationChannels/read|Read notificationchannels.|
|/labs/notificationChannels/write|Add or modify notificationchannels.|
|/labs/policySets/EvaluatePolicies/action|Evaluates lab policy.|
|/labs/policySets/policies/delete|Delete policies.|
|/labs/policySets/policies/read|Read policies.|
|/labs/policySets/policies/write|Add or modify policies.|
|/labs/read|Read labs.|
|/labs/schedules/delete|Delete schedules.|
|/labs/schedules/Execute/action|Execute a schedule.|
|/labs/schedules/ListApplicable/action|Lists all applicable schedules|
|/labs/schedules/read|Read schedules.|
|/labs/schedules/write|Add or modify schedules.|
|/labs/serviceRunners/delete|Delete service runners.|
|/labs/serviceRunners/read|Read service runners.|
|/labs/serviceRunners/write|Add or modify service runners.|
|/labs/users/delete|Delete user profiles.|
|/labs/users/disks/Attach/action|Attach and create the lease of the disk to the virtual machine.|
|/labs/users/disks/delete|Delete disks.|
|/labs/users/disks/Detach/action|Detach and break the lease of the disk attached to the virtual machine.|
|/labs/users/disks/read|Read disks.|
|/labs/users/disks/write|Add or modify disks.|
|/labs/users/environments/delete|Delete environments.|
|/labs/users/environments/read|Read environments.|
|/labs/users/environments/write|Add or modify environments.|
|/labs/users/read|Read user profiles.|
|/labs/users/secrets/delete|Delete secrets.|
|/labs/users/secrets/read|Read secrets.|
|/labs/users/secrets/write|Add or modify secrets.|
|/labs/users/serviceFabrics/delete|Delete service fabrics.|
|/labs/users/serviceFabrics/ListApplicableSchedules/action|Lists all applicable schedules|
|/labs/users/serviceFabrics/read|Read service fabrics.|
|/labs/users/serviceFabrics/schedules/delete|Delete schedules.|
|/labs/users/serviceFabrics/schedules/Execute/action|Execute a schedule.|
|/labs/users/serviceFabrics/schedules/read|Read schedules.|
|/labs/users/serviceFabrics/schedules/write|Add or modify schedules.|
|/labs/users/serviceFabrics/Start/action|Start a service fabric.|
|/labs/users/serviceFabrics/Stop/action|Stop a service fabric|
|/labs/users/serviceFabrics/write|Add or modify service fabrics.|
|/labs/users/write|Add or modify user profiles.|
|/labs/virtualMachines/AddDataDisk/action|Attach a new or existing data disk to virtual machine.|
|/labs/virtualMachines/ApplyArtifacts/action|Apply artifacts to virtual machine.|
|/labs/virtualMachines/Claim/action|Take ownership of an existing virtual machine|
|/labs/virtualMachines/delete|Delete virtual machines.|
|/labs/virtualMachines/DetachDataDisk/action|Detach the specified disk from the virtual machine.|
|/labs/virtualMachines/ListApplicableSchedules/action|Lists all applicable schedules|
|/labs/virtualMachines/read|Read virtual machines.|
|/labs/virtualMachines/Restart/action|Restart a virtual machine.|
|/labs/virtualMachines/schedules/delete|Delete schedules.|
|/labs/virtualMachines/schedules/Execute/action|Execute a schedule.|
|/labs/virtualMachines/schedules/read|Read schedules.|
|/labs/virtualMachines/schedules/write|Add or modify schedules.|
|/labs/virtualMachines/Start/action|Start a virtual machine.|
|/labs/virtualMachines/Stop/action|Stop a virtual machine|
|/labs/virtualMachines/TransferDisks/action|Transfer ownership of virtual machine data disks to yourself|
|/labs/virtualMachines/UnClaim/action|Release ownership of an existing virtual machine|
|/labs/virtualMachines/write|Add or modify virtual machines.|
|/labs/virtualNetworks/delete|Delete virtual networks.|
|/labs/virtualNetworks/read|Read virtual networks.|
|/labs/virtualNetworks/write|Add or modify virtual networks.|
|/labs/write|Add or modify labs.|
|/locations/operations/read|Read operations.|
|/register/action|Registers the subscription|
|/schedules/delete|Delete schedules.|
|/schedules/Execute/action|Execute a schedule.|
|/schedules/read|Read schedules.|
|/schedules/Retarget/action|Updates a schedule's target resource Id.|
|/schedules/write|Add or modify schedules.|

## <a name="microsoftdocumentdb"></a>Microsoft.DocumentDB

| Operation | Description |
|---|---|
|/databaseAccountNames/read|Checks for name availability.|
|/databaseAccounts/changeResourceGroup/action|Change resource group of a database account|
|/databaseAccounts/databases/collections/metricDefinitions/read|Reads the collection metric definitions.|
|/databaseAccounts/databases/collections/metrics/read|Reads the collection metrics.|
|/databaseAccounts/databases/collections/partitionKeyRangeId/metrics/read|Read database account partition key level metrics|
|/databaseAccounts/databases/collections/partitions/metrics/read|Read database account partition level metrics|
|/databaseAccounts/databases/collections/partitions/usages/read|Read database account partition level usages|
|/databaseAccounts/databases/collections/usages/read|Reads the collection usages.|
|/databaseAccounts/databases/metricDefinitions/read|Reads the database metric definitions|
|/databaseAccounts/databases/metrics/read|Reads the database metrics.|
|/databaseAccounts/databases/usages/read|Reads the database usages.|
|/databaseAccounts/delete|Deletes the database accounts.|
|/databaseAccounts/failoverPriorityChange/action|Change failover priorities of regions of a database account. This is used to perform manual failover operation|
|/databaseAccounts/listConnectionStrings/action|Get the connection strings for a database account|
|/databaseAccounts/listKeys/action|List keys of a database account|
|/databaseAccounts/metricDefinitions/read|Reads the database account metrics definitions.|
|/databaseAccounts/metrics/read|Reads the database account metrics.|
|/databaseAccounts/operationResults/read|Read status of the asynchronous operation|
|/databaseAccounts/percentile/metrics/read|Read latency metrics|
|/databaseAccounts/percentile/sourceRegion/targetRegion/metrics/read|Read latency metrics for a specific source and target region|
|/databaseAccounts/percentile/targetRegion/metrics/read|Read latency metrics for a specific target region|
|/databaseAccounts/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/databaseAccounts/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/databaseAccounts/providers/Microsoft.Insights/logDefinitions/read|Gets the available log catageries for Database Account|
|/databaseAccounts/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for the database Account|
|/databaseAccounts/read|Reads a database account.|
|/databaseAccounts/readonlykeys/action|Reads the database account readonly keys.|
|/databaseAccounts/readonlykeys/read|Reads the database account readonly keys.|
|/databaseAccounts/regenerateKey/action|Rotate keys of a database account|
|/databaseAccounts/region/databases/collections/metrics/read|Reads the regional collection metrics.|
|/databaseAccounts/region/databases/collections/partitionKeyRangeId/metrics/read|Read regional database account partition key level metrics|
|/databaseAccounts/region/databases/collections/partitions/metrics/read|Read regional database account partition level metrics|
|/databaseAccounts/region/databases/collections/partitions/read|Read database account partitions in a collection|
|/databaseAccounts/region/metrics/read|Reads the region and database account metrics.|
|/databaseAccounts/usages/read|Reads the database account usages.|
|/databaseAccounts/write|Update a database accounts.|
|/locations/deleteVirtualNetworkOrSubnets/action|Notifies Microsoft.DocumentDB that VirtualNetwork or Subnet is being deleted|
|/operationResults/read|Read status of the asynchronous operation|
|/operations/read|Read operations available for the Microsoft DocumentDB |
|/register/action| Register the Microsoft DocumentDB resource provider for the subscription|

## <a name="microsoftdomainregistration"></a>Microsoft.DomainRegistration

| Operation | Description |
|---|---|
|/checkDomainAvailability/Action|Check if a domain is available for purchase|
|/domains/Delete|Delete an existing domain.|
|/domains/domainownershipidentifiers/Delete|Delete ownership identifier|
|/domains/domainownershipidentifiers/Read|List ownership identifiers|
|/domains/domainownershipidentifiers/Read|Get ownership identifier|
|/domains/domainownershipidentifiers/Write|Create or update identifier|
|/domains/operationresults/Read|Get a domain operation|
|/domains/operations/Read|List all operations from app service domain registration|
|/domains/Read|Get the list of domains|
|/domains/Read|Get domain|
|/domains/renew/Action|Renew an existing domain.|
|/domains/Write|Add a new Domain or update an existing one|
|/generateSsoRequest/Action|Generate a request for signing into domain control center.|
|/listDomainRecommendations/Action|Retrieve the list domain recommendations based on keywords|
|/register/action|Register the Microsoft Domains resource provider for the subscription|
|/topLevelDomains/listAgreements/Action|List Agreement action|
|/topLevelDomains/Read|Get toplevel domains|
|/topLevelDomains/Read|Get toplevel domain|
|/validateDomainRegistrationInformation/Action|Validate domain purchase object without submitting it|

## <a name="microsoftdynamicslcs"></a>Microsoft.DynamicsLcs

| Operation | Description |
|---|---|
|/lcsprojects/clouddeployments/read|Display Microsoft Dynamics AX 2012 R3 Evaluation deployments in a Microsoft Dynamics Lifecycle Services project that belong to a user|
|/lcsprojects/clouddeployments/write|Create Microsoft Dynamics AX 2012 R3 Evaluation deployment in a Microsoft Dynamics Lifecycle Services project that belong to a user. Deployments can be managed from Azure management portal|
|/lcsprojects/connectors/read|Read connectors that belong to a Microsoft Dynamics Lifecycle Services project|
|/lcsprojects/connectors/write|Create and update connectors that belong to a Microsoft Dynamics Lifecycle Services project|
|/lcsprojects/delete|Delete Microsoft Dynamics Lifecycle Services projects that belong to the user|
|/lcsprojects/read|Display Microsoft Dynamics Lifecycle Services projects that belong to a user|
|/lcsprojects/write|Create and update Microsoft Dynamics Lifecycle Services projects that belong to the user. Only the name and description properties can be updated. The subscription and location associated with the project cannot be updated after creation|

## <a name="microsofteventgrid"></a>Microsoft.EventGrid

| Operation | Description |
|---|---|
|/eventSubscriptions/delete|Delete a eventSubscription|
|/eventSubscriptions/getFullUrl/action|Get full url for the event subscription|
|/eventSubscriptions/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for event subscriptions|
|/eventSubscriptions/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for event subscriptions|
|/eventSubscriptions/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for eventSubscriptions|
|/eventSubscriptions/read|Read a eventSubscription|
|/eventSubscriptions/write|Create or update a eventSubscription|
|/extensionTopics/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for topics|
|/extensionTopics/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for topics|
|/extensionTopics/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for topics|
|/register/action|Registers the eventSubscription for the EventGrid resource provider and enables the creation of Event Grid subscriptions.|
|/topics/delete|Delete a topic|
|/topics/listKeys/action|List keys for the topic|
|/topics/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for topics|
|/topics/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for topics|
|/topics/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for topics|
|/topics/read|Read a topic|
|/topics/regenerateKey/action|Regenerate key for the topic|
|/topics/write|Create or update a topic|

## <a name="microsofteventhub"></a>Microsoft.EventHub

| Operation | Description |
|---|---|
|/checkNameAvailability/action|Checks availability of namespace under given subscription.|
|/checkNamespaceAvailability/action|Checks availability of namespace under given subscription. This API is deprecated please use CheckNameAvailabiltiy instead.|
|/namespaces/authorizationRules/action|Updates Namespace Authorization Rule. This API is depricated. Please use a PUT call to update the Namespace Authorization Rule instead.. This operation is not supported on API version 2017-04-01.|
|/namespaces/authorizationRules/delete|Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted. |
|/namespaces/authorizationRules/listkeys/action|Get the Connection String to the Namespace|
|/namespaces/authorizationRules/read|Get the list of Namespaces Authorization Rules description.|
|/namespaces/authorizationRules/regenerateKeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/authorizationRules/write|Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated.|
|/namespaces/Delete|Delete Namespace Resource|
|/namespaces/disasterRecoveryConfigs/authorizationRules/listkeys/action|Gets the authorization rules keys for the Disaster Recovery primary namespace|
|/namespaces/disasterRecoveryConfigs/authorizationRules/read|Get Disaster Recovery Primary Namespace's Authorization Rules|
|/namespaces/disasterRecoveryConfigs/breakPairing/action|Disables Disaster Recovery and stops replicating changes from primary to secondary namespaces.|
|/namespaces/disasterrecoveryconfigs/checkNameAvailability/action|Checks availability of namespace alias under given subscription.|
|/namespaces/disasterRecoveryConfigs/delete|Deletes the Disaster Recovery configuration associated with the namespace. This operation can only be invoked via the primary namespace.|
|/namespaces/disasterRecoveryConfigs/failover/action|Invokes a GEO DR failover and reconfigures the namespace alias to point to the secondary namespace.|
|/namespaces/disasterRecoveryConfigs/read|Gets the Disaster Recovery configuration associated with the namespace.|
|/namespaces/disasterRecoveryConfigs/write|Creates or Updates the Disaster Recovery configuration associated with the namespace.|
|/namespaces/eventhubs/authorizationRules/action|Operation to update EventHub. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule.|
|/namespaces/eventhubs/authorizationRules/delete|Operation to delete EventHub Authorization Rules|
|/namespaces/eventhubs/authorizationRules/listkeys/action|Get the Connection String to EventHub|
|/namespaces/eventhubs/authorizationRules/read| Get the list of EventHub Authorization Rules|
|/namespaces/eventhubs/authorizationRules/regenerateKeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/eventhubs/authorizationRules/write|Create EventHub Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated.|
|/namespaces/eventHubs/consumergroups/Delete|Operation to delete ConsumerGroup Resource|
|/namespaces/eventHubs/consumergroups/read|Get list of ConsumerGroup Resource Descriptions|
|/namespaces/eventHubs/consumergroups/write|Create or Update ConsumerGroup properties.|
|/namespaces/eventhubs/Delete|Operation to delete EventHub Resource|
|/namespaces/eventhubs/read|Get list of EventHub Resource Descriptions|
|/namespaces/eventhubs/write|Create or Update EventHub properties.|
|/namespaces/messagingPlan/read|Gets the Messaging Plan for a namespace. This API is deprecated. Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions.. This operation is not supported on API version 2017-04-01.|
|/namespaces/messagingPlan/write|Updates the Messaging Plan for a namespace. This API is deprecated. Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions.. This operation is not supported on API version 2017-04-01.|
|/namespaces/operationresults/read|Get the status of Namespace operation|
|/namespaces/providers/Microsoft.Insights/diagnosticSettings/read|Get list of Namespace diagnostic settings Resource Descriptions|
|/namespaces/providers/Microsoft.Insights/diagnosticSettings/write|Get list of Namespace diagnostic settings Resource Descriptions|
|/namespaces/providers/Microsoft.Insights/logDefinitions/read|Get list of Namespace logs Resource Descriptions|
|/namespaces/providers/Microsoft.Insights/metricDefinitions/read|Get list of Namespace metrics Resource Descriptions|
|/namespaces/read|Get the list of Namespace Resource Description|
|/namespaces/write|Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated.|
|/operations/read|Get Operations|
|/register/action|Registers the subscription for the EventHub resource provider and enables the creation of EventHub resources|
|/sku/read|Get list of Sku Resource Descriptions|
|/sku/regions/read|Get list of SkuRegions Resource Descriptions|
|/unregister/action|Registers the EventHub Resource Provider|

## <a name="microsoftfeatures"></a>Microsoft.Features

| Operation | Description |
|---|---|
|/features/read|Gets the features of a subscription.|
|/providers/features/read|Gets the feature of a subscription in a given resource provider.|
|/providers/features/register/action|Registers the feature for a subscription in a given resource provider.|
|/providers/features/unregister/action|Unregisters the feature for a subscription in a given resource provider.|

## <a name="microsofthdinsight"></a>Microsoft.HDInsight

| Operation | Description |
|---|---|
|/clusters/changerdpsetting/action|Change RDP setting for HDInsight Cluster|
|/clusters/configurations/action|Update HDInsight Cluster Configuration|
|/clusters/configurations/read|Get HDInsight Cluster Configurations|
|/clusters/delete|Delete a HDInsight Cluster|
|/clusters/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource HDInsight Cluster|
|/clusters/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource HDInsight Cluster|
|/clusters/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for HDInsight Cluster|
|/clusters/read|Get details about HDInsight Cluster|
|/clusters/roles/resize/action|Resize a HDInsight Cluster|
|/clusters/write|Create or Update HDInsight Cluster|
|/locations/capabilities/read|Get Subscription Capabilities|
|/locations/checkNameAvailability/read|Check Name Availability|

## <a name="microsoftimportexport"></a>Microsoft.ImportExport

| Operation | Description |
|---|---|
|/jobs/delete|Deletes an existing job.|
|/jobs/listBitLockerKeys/action|Gets the BitLocker keys for the specified job.|
|/jobs/read|Gets the properties for the specified job or returns the list of jobs.|
|/jobs/write|Creates a job with the specified parameters or update the properties or tags for the specified job.|
|/locations/read|Gets the properties for the specified location or returns the list of locations.|
|/register/action|Registers the subscription for the import/export resource provider and enables the creation of import/export jobs.|

## <a name="microsoftinsights"></a>Microsoft.Insights

| Operation | Description |
|---|---|
|/ActionGroups/Delete|Deleting an action group|
|/ActionGroups/Read|Reading an action group|
|/ActionGroups/Write|Writing an action group|
|/ActivityLogAlerts/Activated/Action|Triggered the Activity Log Alert|
|/ActivityLogAlerts/Delete|Deleting an activity log alert|
|/ActivityLogAlerts/Read|Reading an activity log alert|
|/ActivityLogAlerts/Write|Reading an activity log alert|
|/AlertRules/Activated/Action|Alert Rule activated|
|/AlertRules/Delete|Deleting an alert rule configuration|
|/AlertRules/Incidents/Read|Reading an alert rule incident configuration|
|/AlertRules/Read|Reading an alert rule configuration|
|/AlertRules/Resolved/Action|Alert Rule resolved|
|/AlertRules/Throttled/Action|Alert rule is throttled|
|/AlertRules/Write|Writing to an alert rule configuration|
|/AutoscaleSettings/Delete|Deleting an autoscale setting configuration|
|/AutoscaleSettings/providers/Microsoft.Insights/MetricDefinitions/Read|Read metric definitions|
|/AutoscaleSettings/Read|Reading an autoscale setting configuration|
|/AutoscaleSettings/Scaledown/Action|Autoscale scale down operation|
|/AutoscaleSettings/Scaleup/Action|Autoscale scale up operation|
|/AutoscaleSettings/Write|Writing to an autoscale setting configuration|
|/Components/AnalyticsItems/Delete|Deleting an Application Insights analytics item|
|/Components/AnalyticsItems/Read|Reading an Application Insights analytics item|
|/Components/AnalyticsItems/Write|Writing an Application Insights analytics item|
|/Components/AnalyticsTables/Action|Application Insights analytics table action|
|/Components/AnalyticsTables/Delete|Deleting an Application Insights analytics table schema|
|/Components/AnalyticsTables/Read|Reading an Application Insights analytics table schema|
|/Components/AnalyticsTables/Write|Writing an Application Insights analytics table schema|
|/Components/Annotations/Delete|Deleting an Application Insights annotation|
|/Components/Annotations/Read|Reading an Application Insights annotation|
|/Components/Annotations/Write|Writing an Application Insights annotation|
|/Components/Api/Read|Reading Application Insights component data API|
|/Components/ApiKeys/Action|Generating an Application Insights API key|
|/Components/ApiKeys/Delete|Deleting an Application Insights API key|
|/Components/ApiKeys/Read|Reading an Application Insights API key|
|/Components/BillingPlanForComponent/Read|Reading a billing plan for Application Insights component|
|/Components/CurrentBillingFeatures/Read|Reading current billing features for Application Insights component|
|/Components/CurrentBillingFeatures/Write|Writing current billing features for Application Insights component|
|/Components/DefaultWorkItemConfig/Read|Reading an Application Insights default ALM integration configuration|
|/Components/Delete|Deleting an application insights component configuration|
|/Components/ExportConfiguration/Action|Application Insights export settings action|
|/Components/ExportConfiguration/Delete|Deleting Application Insights export settings|
|/Components/ExportConfiguration/Read|Reading Application Insights export settings|
|/Components/ExportConfiguration/Write|Writing Application Insights export settings|
|/Components/ExtendQueries/Read|Reading Application Insights component extended query results|
|/Components/Favorites/Delete|Deleting an Application Insights favorite|
|/Components/Favorites/Read|Reading an Application Insights favorite|
|/Components/Favorites/Write|Writing an Application Insights favorite|
|/Components/FeatureCapabilities/Read|Reading Application Insights component feature capabilities|
|/Components/GetAvailableBillingFeatures/Read|Reading Application Insights component available billing features|
|/Components/GetToken/Read|Reading an Application Insights component token|
|/Components/ListMigrationDate/Action|Get back Subscription migration date|
|/Components/ListMigrationDate/Read|Get back subscription migration date|
|/Components/MetricDefinitions/Read|Reading Application Insights component metric definitions|
|/Components/Metrics/Read|Reading Application Insights component metrics|
|/Components/MigrateToNewpricingModel/Action|Migrate subscription to new pricing model|
|/Components/Move/Action|Move an Application Insights Component to another resource group or subscription|
|/Components/MyAnalyticsItems/Delete|Deleting an Application Insights personal analytics item|
|/Components/MyAnalyticsItems/Read|Reading an Application Insights personal analytics item|
|/Components/MyAnalyticsItems/Write|Writing an Application Insights personal analytics item|
|/Components/MyFavorites/Read|Reading an Application Insights personal favorite|
|/Components/PricingPlans/Read|Reading an Application Insights component pricing plan|
|/Components/PricingPlans/Write|Writing an Application Insights component pricing plan|
|/Components/ProactiveDetectionConfigs/Read|Reading Application Insights proactive detection configuration|
|/Components/ProactiveDetectionConfigs/Write|Writing Application Insights proactive detection configuration|
|/Components/providers/Microsoft.Insights/MetricDefinitions/Read|Read metric definitions|
|/Components/QuotaStatus/Read|Reading Application Insights component quota status|
|/Components/Read|Reading an application insights component configuration|
|/Components/RollbackToLegacyPricingModel/Action|Rollback subscription to legacy pricing model|
|/Components/SyntheticMonitorLocations/Read|Reading Application Insights webtest locations|
|/Components/WorkItemConfigs/Delete|Deleting an Application Insights ALM integration configuration|
|/Components/WorkItemConfigs/Read|Reading an Application Insights ALM integration configuration|
|/Components/WorkItemConfigs/Write|Writing an Application Insights ALM integration configuration|
|/Components/Write|Writing to an application insights component configuration|
|/DiagnosticSettings/Delete|Deleting diagnostic settings configuration|
|/DiagnosticSettings/Read|Reading a diagnostic settings configuration|
|/DiagnosticSettings/Write|Writing to diagnostic settings configuration|
|/EventCategories/Read|Reading an event category|
|/eventtypes/digestevents/Read|Read management event type digest|
|/eventtypes/values/Read|Read management event type values|
|/ExtendedDiagnosticSettings/Delete|Deleting extended diagnostic settings configuration|
|/ExtendedDiagnosticSettings/Read|Reading a extended diagnostic settings configuration|
|/ExtendedDiagnosticSettings/Write|Writing to extended diagnostic settings configuration|
|/LogDefinitions/Read|Read log definitions|
|/LogProfiles/Delete|Delete log profiles configuration|
|/LogProfiles/Read|Read log profiles|
|/LogProfiles/Write|Writing to a log profile configuration|
|/MetricAlerts/Delete|Deleting a metric alert|
|/MetricAlerts/Read|Reading a metric alert|
|/MetricAlerts/Write|Writing a metric alert|
|/MetricDefinitions/Microsoft.Insights/Read|Read metric definitions|
|/MetricDefinitions/providers/Microsoft.Insights/Read|Read metric definitions|
|/MetricDefinitions/Read|Read metric definitions|
|/Metrics/providers/Metrics/Read|Read metrics|
|/Metrics/Read|Read metrics|
|/Metrics/Write|Write metrics|
|/Operations/Read|Reading operations|
|/Register/Action|Register the microsoft insights provider|
|/Tenants/Register/Action|Initializes the microsoft insights provider|
|/Unregister/Action|Register the microsoft insights provider|
|/Webtests/Delete|Deleting a webtest configuration|
|/Webtests/GetToken/Read|Reading a webtest token|
|/Webtests/MetricDefinitions/Read|Reading a webtest metric definitions|
|/Webtests/Metrics/Read|Reading a webtest metrics|
|/Webtests/Read|Reading a webtest configuration|
|/Webtests/Write|Writing to a webtest configuration|

## <a name="microsoftkeyvault"></a>Microsoft.KeyVault

| Operation | Description |
|---|---|
|/checkNameAvailability/read|Checks that a key vault name is valid and is not in use|
|/deletedVaults/read|View the properties of soft deleted key vaults|
|/hsmPools/delete|Delete an HSM pool|
|/hsmPools/joinVault/action|Join a key vault to an HSM pool|
|/hsmPools/read|View the properties of an HSM pool|
|/hsmPools/write|Create a new HSM pool of update the properties of an existing HSM pool|
|/locations/deletedVaults/purge/action|Purge a soft deleted key vault|
|/locations/deletedVaults/read|View the properties of a soft deleted key vault|
|/locations/deleteVirtualNetworkOrSubnets/action|Notifies Microsoft.KeyVault that a virtual network or subnet is being deleted|
|/locations/operationResults/read|Check the result of a long run operation|
|/operations/read|Lists operations available on Microsoft.KeyVault resource provider|
|/register/action|Registers a subscription|
|/unregister/action|Unregisters a subscription|
|/vaults/accessPolicies/write|Update an existing access policy by merging or replacing, or add a new access policy to a vault.|
|/vaults/delete|Delete a key vault|
|/vaults/deploy/action|Enables access to secrets in a key vault when deploying Azure resources|
|/vaults/providers/Microsoft.Insights/diagnosticSettings/Read|Gets the diagnostic setting for the resource|
|/vaults/providers/Microsoft.Insights/diagnosticSettings/Write|Creates or updates the diagnostic setting for the resource|
|/vaults/providers/Microsoft.Insights/logDefinitions/read|Gets the available logs for a key vault|
|/vaults/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for a key vault|
|/vaults/read|View the properties of a key vault|
|/vaults/secrets/read|View the properties of a secret, but not its value|
|/vaults/secrets/write|Create a new secret or update the value of an existing secret|
|/vaults/write|Create a new key vault or update the properties of an existing key vault|

## <a name="microsoftlabservices"></a>Microsoft.LabServices

| Operation | Description |
|---|---|
|/labAccounts/CreateLab/action|Create a lab in a lab account.|
|/labAccounts/delete|Delete lab accounts.|
|/labAccounts/labs/delete|Delete labs.|
|/labAccounts/labs/environmentSettings/delete|Delete environment setting.|
|/labAccounts/labs/environmentSettings/environments/delete|Delete environments.|
|/labAccounts/labs/environmentSettings/environments/read|Read environments.|
|/labAccounts/labs/environmentSettings/environments/write|Add or modify environments.|
|/labAccounts/labs/environmentSettings/Publish/action|Provisions/deprovisions required resources for an environment setting based on current state of the lab/environment setting.|
|/labAccounts/labs/environmentSettings/read|Read environment setting.|
|/labAccounts/labs/environmentSettings/write|Add or modify environment setting.|
|/labAccounts/labs/read|Read labs.|
|/labAccounts/labs/users/delete|Delete users.|
|/labAccounts/labs/users/read|Read users.|
|/labAccounts/labs/users/write|Add or modify users.|
|/labAccounts/labs/write|Add or modify labs.|
|/labAccounts/read|Read lab accounts.|
|/labAccounts/write|Add or modify lab accounts.|
|/locations/operations/read|Read operations.|
|/register/action|Registers the subscription|

## <a name="microsoftlocationbasedservices"></a>Microsoft.LocationBasedServices

| Operation | Description |
|---|---|
|/accounts/delete|Delete a Location Based Services Account.|
|/accounts/listKeys/action|List Location Based Services Account keys|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/accounts/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/accounts/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Location Based Services Accounts|
|/accounts/read|Get a Location Based Services Account.|
|/accounts/regenerateKey/action|Generate new Location Based Services Account primary or secondary key|
|/accounts/write|Create or update a Location Based Services Account.|
|/register/action|Register the provider|

## <a name="microsoftlogic"></a>Microsoft.Logic

| Operation | Description |
|---|---|
|/integrationAccounts/agreements/delete|Deletes the agreement in integration account.|
|/integrationAccounts/agreements/listContentCallbackUrl/action|Gets the callback URL for agreement content in integration account.|
|/integrationAccounts/agreements/read|Reads the agreement in integration account.|
|/integrationAccounts/agreements/write|Creates or updates the agreement in integration account.|
|/integrationAccounts/assemblies/delete|Deletes the assembly in integration account.|
|/integrationAccounts/assemblies/listContentCallbackUrl/action|Gets the callback URL for assembly content in integration account.|
|/integrationAccounts/assemblies/read|Reads the assembly in integration account.|
|/integrationAccounts/assemblies/write|Creates or updates the assembly in integration account.|
|/integrationAccounts/batchConfigurations/delete|Deletes the batch configuration in integration account.|
|/integrationAccounts/batchConfigurations/read|Reads the batch configuration in integration account.|
|/integrationAccounts/batchConfigurations/write|Creates or updates the batch configuration in integration account.|
|/integrationAccounts/certificates/delete|Deletes the certificate in integration account.|
|/integrationAccounts/certificates/read|Reads the certificate in integration account.|
|/integrationAccounts/certificates/write|Creates or updates the certificate in integration account.|
|/integrationAccounts/delete|Deletes the integration account.|
|/integrationAccounts/listCallbackUrl/action|Gets the callback URL for integration account.|
|/integrationAccounts/listKeyVaultKeys/action|Gets the keys in the key vault.|
|/integrationAccounts/logTrackingEvents/action|Logs the tracking events in the integration account.|
|/integrationAccounts/maps/delete|Deletes the map in integration account.|
|/integrationAccounts/maps/listContentCallbackUrl/action|Gets the callback URL for map content in integration account.|
|/integrationAccounts/maps/read|Reads the map in integration account.|
|/integrationAccounts/maps/write|Creates or updates the map in integration account.|
|/integrationAccounts/partners/delete|Deletes the partner in integration account.|
|/integrationAccounts/partners/listContentCallbackUrl/action|Gets the callback URL for partner content in integration account.|
|/integrationAccounts/partners/read|Reads the parter in integration account.|
|/integrationAccounts/partners/write|Creates or updates the partner in integration account.|
|/integrationAccounts/providers/Microsoft.Insights/logDefinitions/read|Reads the Integration Account log definitions.|
|/integrationAccounts/read|Reads the integration account.|
|/integrationAccounts/regenerateAccessKey/action|Regenerates the access key secrets.|
|/integrationAccounts/schemas/delete|Deletes the schema in integration account.|
|/integrationAccounts/schemas/listContentCallbackUrl/action|Gets the callback URL for schema content in integration account.|
|/integrationAccounts/schemas/read|Reads the schema in integration account.|
|/integrationAccounts/schemas/write|Creates or updates the schema in integration account.|
|/integrationAccounts/sessions/delete|Deletes the session in integration account.|
|/integrationAccounts/sessions/read|Reads the batch configuration in integration account.|
|/integrationAccounts/sessions/write|Creates or updates the session in integration account.|
|/integrationAccounts/write|Creates or updates the integration account.|
|/locations/workflows/validate/action|Validates the workflow.|
|/operations/read|Gets the operation.|
|/register/action|Registers the Microsoft.Logic resource provider for a given subscription.|
|/workflows/accessKeys/delete|Deletes the access key.|
|/workflows/accessKeys/list/action|Lists the access key secrets.|
|/workflows/accessKeys/read|Reads the access key.|
|/workflows/accessKeys/regenerate/action|Regenerates the access key secrets.|
|/workflows/accessKeys/write|Creates or updates the access key.|
|/workflows/delete|Deletes the workflow.|
|/workflows/disable/action|Disables the workflow.|
|/workflows/enable/action|Enables the workflow.|
|/workflows/listCallbackUrl/action|Gets the callback URL for workflow.|
|/workflows/listSwagger/action|Gets the workflow swagger definitions.|
|/workflows/move/action|Moves Workflow from its existing subscription id, resource group, and/or name to a different subscription id, resource group, and/or name.|
|/workflows/providers/Microsoft.Insights/diagnosticSettings/read|Reads the workflow diagnostic settings.|
|/workflows/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the workflow diagnostic setting.|
|/workflows/providers/Microsoft.Insights/logDefinitions/read|Reads the workflow log definitions.|
|/workflows/providers/Microsoft.Insights/metricDefinitions/read|Reads the workflow metric definitions.|
|/workflows/read|Reads the workflow.|
|/workflows/regenerateAccessKey/action|Regenerates the access key secrets.|
|/workflows/run/action|Starts a run of the workflow.|
|/workflows/runs/actions/listExpressionTraces/action|Gets the workflow run action expression traces.|
|/workflows/runs/actions/read|Reads the workflow run action.|
|/workflows/runs/actions/repetitions/listExpressionTraces/action|Gets the workflow run action repetition expression traces.|
|/workflows/runs/actions/repetitions/read|Reads the workflow run action repetition.|
|/workflows/runs/actions/scoperepetitions/read|Reads the workflow run action scope repetition.|
|/workflows/runs/cancel/action|Cancels the run of a workflow.|
|/workflows/runs/operations/read|Reads the workflow run operation status.|
|/workflows/runs/read|Reads the workflow run.|
|/workflows/suspend/action|Suspends the workflow.|
|/workflows/triggers/histories/read|Reads the trigger histories.|
|/workflows/triggers/histories/resubmit/action|Resubmits the workflow trigger.|
|/workflows/triggers/listCallbackUrl/action|Gets the callback URL for trigger.|
|/workflows/triggers/read|Reads the trigger.|
|/workflows/triggers/reset/action|Resets the trigger.|
|/workflows/triggers/run/action|Executes the trigger.|
|/workflows/triggers/setState/action|Sets the trigger state.|
|/workflows/validate/action|Validates the workflow.|
|/workflows/versions/read|Reads the workflow version.|
|/workflows/versions/triggers/listCallbackUrl/action|Gets the callback URL for trigger.|
|/workflows/write|Creates or updates the workflow.|

## <a name="microsoftmachinelearning"></a>Microsoft.MachineLearning

| Operation | Description |
|---|---|
|/commitmentPlans/commitmentAssociations/move/action|Move any Machine Learning Commitment Plan Association|
|/commitmentPlans/commitmentAssociations/read|Read any Machine Learning Commitment Plan Association|
|/commitmentPlans/delete|Delete any Machine Learning Commitment Plan|
|/commitmentPlans/join/action|Join any Machine Learning Commitment Plan|
|/commitmentPlans/read|Read any Machine Learning Commitment Plan|
|/commitmentPlans/write|Create or Update any Machine Learning Commitment Plan|
|/locations/operationresults/read|Get result of a Machine Learning Operation|
|/locations/operationsstatus/read|Get status of an ongoing Machine Learning Operation|
|/operations/read|Get Machine Learning Operations|
|/register/action|Registers the subscription for the machine learning web service resource provider and enables the creation of web services.|
|/skus/read|Get Machine Learning Commitment Plan SKUs|
|/webServices/action|Create regional Web Service Properties for supported regions|
|/webServices/delete|Delete any Machine Learning Web Service|
|/webServices/read|Read any Machine Learning Web Service|
|/webServices/write|Create or Update any Machine Learning Web Service|
|/Workspaces/delete|Delete any Machine Learning Workspace|
|/Workspaces/listworkspacekeys/action|List keys for a Machine Learning Workspace|
|/Workspaces/read|Read any Machine Learning Workspace|
|/Workspaces/resyncstoragekeys/action|Resync keys of storage account configured for a Machine Learning Workspace|
|/Workspaces/write|Create or Update any Machine Learning Workspace|

## <a name="microsoftmachinelearningcompute"></a>Microsoft.MachineLearningCompute

| Operation | Description |
|---|---|
|/operationalizationClusters/checkUpdate/action|Check if updates are available for system services for the operationalization cluster|
|/operationalizationClusters/delete|Delete any hosting account|
|/operationalizationClusters/listKeys/action|List the keys associated with operationalization cluster|
|/operationalizationClusters/read|Read any hosting account|
|/operationalizationClusters/updateSystem/action|Update the system services in an operationalization cluster|
|/operationalizationClusters/write|Create or update any hosting account|
|/register/action|Registers subscription ID to the resource provider and enables the creation of a machine learning compute resources|

## <a name="microsoftmachinelearningmodelmanagement"></a>Microsoft.MachineLearningModelManagement

| Operation | Description |
|---|---|
|/accounts/delete|Delete any hosting account|
|/accounts/read|Read any hosting account|
|/accounts/write|Create or update any hosting account|
|/register/action|Registers subscription ID to the resource provider and enables the creation of a hosting account|

## <a name="microsoftmanagedidentity"></a>Microsoft.ManagedIdentity

| Operation | Description |
|---|---|
|/userAssignedIdentities/assign/action|RBAC action for assigning an existing user assigned identity to a resource|
|/userAssignedIdentities/delete|Deletes an existing user assigned identity|
|/userAssignedIdentities/read|Gets an existing user assigned identity|
|/userAssignedIdentities/write|Creates a new user assigned identity or updates the tags associated with an existing user assigned identity|

## <a name="microsoftmanagedlab"></a>Microsoft.ManagedLab

| Operation | Description |
|---|---|
|/labAccounts/CreateLab/action|Create a lab in a lab account.|
|/labAccounts/delete|Delete lab accounts.|
|/labAccounts/labs/delete|Delete labs.|
|/labAccounts/labs/environmentSettings/delete|Delete environment setting.|
|/labAccounts/labs/environmentSettings/environments/delete|Delete environments.|
|/labAccounts/labs/environmentSettings/environments/read|Read environments.|
|/labAccounts/labs/environmentSettings/environments/write|Add or modify environments.|
|/labAccounts/labs/environmentSettings/read|Read environment setting.|
|/labAccounts/labs/environmentSettings/write|Add or modify environment setting.|
|/labAccounts/labs/labVms/delete|Delete lab virtual machines.|
|/labAccounts/labs/labVms/read|Read lab virtual machines.|
|/labAccounts/labs/labVms/write|Add or modify lab virtual machines.|
|/labAccounts/labs/read|Read labs.|
|/labAccounts/labs/write|Add or modify labs.|
|/labAccounts/read|Read lab accounts.|
|/labAccounts/write|Add or modify lab accounts.|
|/locations/operations/read|Read operations.|
|/register/action|Registers the subscription|

## <a name="microsoftmanagement"></a>Microsoft.Management

| Operation | Description |
|---|---|
|/checkNameAvailability/action|Checks if the specified management group name is valid and unique.|
|/getEntities/action|List all entities (Management Groups, Subscriptions, etc.) for the authenticated user.|
|/managementGroups/delete|Delete management group.|
|/managementGroups/read|List management groups for the authenticated user.|
|/managementGroups/subscriptions/delete|De-associates subscription from the management group.|
|/managementGroups/subscriptions/write|Associates existing subscription with the management group.|
|/managementGroups/write|Create or update a management group.|

## <a name="microsoftmarketplaceapps"></a>Microsoft.MarketplaceApps

| Operation | Description |
|---|---|
|/ClassicDevServices/delete|Does a DELETE operation on a classic dev service resource.|
|/ClassicDevServices/listSecrets/action|Gets a classic dev service resource management keys.|
|/ClassicDevServices/listSingleSignOnToken/action|Gets the Single Sign On URL for a classic dev service.|
|/ClassicDevServices/read|Does a GET operation on a classic dev service.|
|/ClassicDevServices/regenerateKey/action|Generates a classic dev service resource management keys.|
|/Operations/read|Read the operations for all resource types.|

## <a name="microsoftmarketplaceordering"></a>Microsoft.MarketplaceOrdering

| Operation | Description |
|---|---|
|/agreements/offers/plans/cancel/action|Cancel an agreement for a given marketplace item|
|/agreements/offers/plans/read|Return an agreement for a given marketplace item|
|/agreements/offers/plans/sign/action|Sign an agreement for a given marketplace item|
|/agreements/read|Return all agreements under given subscription|
|/offertypes/publishers/offers/plans/agreements/read|Get an agreement for a given marketplace virtual machine item|
|/offertypes/publishers/offers/plans/agreements/write|Sign or Cancel an agreement for a given marketplace virtual machine item|

## <a name="microsoftmedia"></a>Microsoft.Media

| Operation | Description |
|---|---|
|/checknameavailability/action|Checks if a Media Services account name is available|
|/mediaservices/delete|Delete any Media Services Account|
|/mediaservices/listKeys/action|List the ACS keys for the Media Services account|
|/mediaservices/read|Read any Media Services Account|
|/mediaservices/regenerateKey/action|Regenerate a Media Services ACS key|
|/mediaservices/syncStorageKeys/action|Synchronize the Storage Keys for an attached Azure Storage account|
|/mediaservices/write|Create or Update any Media Services Account|
|/operations/read|Read any Media Services Account|
|/register/action|Registers the subscription for the Media Services resource provider and enables the creation of Media Services accounts|

## <a name="microsoftmigrate"></a>Microsoft.Migrate

| Operation | Description |
|---|---|
|/Operations/read|Reads the exposed operations|

## <a name="microsoftnetwork"></a>Microsoft.Network

| Operation | Description |
|---|---|
|/applicationGatewayAvailableSslOptions/predefinedPolicies/read|Application Gateway Ssl Predefined Policy|
|/applicationGatewayAvailableSslOptions/read|Application Gateway available Ssl Options|
|/applicationGatewayAvailableWafRuleSets/read|Gets Application Gateway Available Waf Rule Sets|
|/applicationGateways/backendAddressPools/join/action|Joins an application gateway backend address pool|
|/applicationGateways/backendhealth/action|Gets an application gateway backend health|
|/applicationGateways/delete|Deletes an application gateway|
|/applicationGateways/effectiveNetworkSecurityGroups/action|Get Route Table configured On Application Gateway|
|/applicationGateways/effectiveRouteTable/action|Get Route Table configured On Application Gateway|
|/applicationGateways/providers/Microsoft.Insights/logDefinitions/read|Gets the events for Application Gateway|
|/applicationGateways/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Application Gateway|
|/applicationGateways/read|Gets an application gateway|
|/applicationGateways/setSecurityCenterConfiguration/action|Sets Application Gateway Security Center Configuration|
|/applicationGateways/start/action|Starts an application gateway|
|/applicationGateways/stop/action|Stops an application gateway|
|/applicationGateways/write|Creates an application gateway or updates an application gateway|
|/applicationSecurityGroups/delete|Deletes an Application Security Group|
|/applicationSecurityGroups/joinIpConfiguration/action|Joins an IP Configuration to Application Security Groups.|
|/applicationSecurityGroups/joinNetworkSecurityRule/action|Joins a Security Rule to Application Security Groups.|
|/applicationSecurityGroups/read|Gets an Application Security Group ID.|
|/applicationSecurityGroups/write|Creates an Application Security Group, or updates an existing Application Security Group.|
|/bgpServiceCommunities/read|Get Bgp Service Communities|
|/checkTrafficManagerNameAvailability/action|Checks the availability of a Traffic Manager Relative DNS name.|
|/connections/delete|Deletes VirtualNetworkGatewayConnection|
|/connections/read|Gets VirtualNetworkGatewayConnection|
|/connections/sharedkey/action|Get VirtualNetworkGatewayConnection SharedKey|
|/connections/sharedKey/read|Gets VirtualNetworkGatewayConnection SharedKey|
|/connections/sharedKey/write|Creates or updates an existing VirtualNetworkGatewayConnection SharedKey|
|/connections/vpndeviceconfigurationscript/read|Gets Vpn Device Configuration of VirtualNetworkGatewayConnection|
|/connections/write|Creates or updates an existing VirtualNetworkGatewayConnection|
|/ddosProtectionPlans/ddosProtectionPlanProxies/delete|Deletes a DDoS Protection Plan Proxy|
|/ddosProtectionPlans/ddosProtectionPlanProxies/read|Gets a DDoS Protection Plan Proxy definition|
|/ddosProtectionPlans/ddosProtectionPlanProxies/write|Creates a DDoS Protection Plan Proxy or updates and existing DDoS Protection Plan Proxy|
|/ddosProtectionPlans/delete|Deletes a DDoS Protection Plan|
|/ddosProtectionPlans/join/action|Joins a DDoS Protection Plan|
|/ddosProtectionPlans/read|Gets a DDoS Protection Plan|
|/ddosProtectionPlans/write|Creates a DDoS Protection Plan or updates a DDoS Protection Plan |
|/dnsoperationresults/read|Gets results of a DNS operation|
|/dnsoperationstatuses/read|Gets status of a DNS operation |
|/dnszones/A/delete|Remove the record set of a given name and type ‘A’ from a DNS zone.|
|/dnszones/A/read|Get the record set of type ‘A’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag.|
|/dnszones/A/write|Create or update a record set of type ‘A’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/AAAA/delete|Remove the record set of a given name and type ‘AAAA’ from a DNS zone.|
|/dnszones/AAAA/read|Get the record set of type ‘AAAA’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag.|
|/dnszones/AAAA/write|Create or update a record set of type ‘AAAA’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/all/read|Gets DNS record sets across types|
|/dnszones/CAA/delete|Remove the record set of a given name and type ‘CAA’ from a DNS zone.|
|/dnszones/CAA/read|Get the record set of type ‘CAA’, in JSON format. The record set contains the TTL, tags, and etag.|
|/dnszones/CAA/write|Create or update a record set of type ‘CAA’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/CNAME/delete|Remove the record set of a given name and type ‘CNAME’ from a DNS zone.|
|/dnszones/CNAME/read|Get the record set of type ‘CNAME’, in JSON format. The record set contains the TTL, tags, and etag.|
|/dnszones/CNAME/write|Create or update a record set of type ‘CNAME’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/delete|Delete the DNS zone, in JSON format. The zone properties include tags, etag, numberOfRecordSets, and maxNumberOfRecordSets.|
|/dnszones/MX/delete|Remove the record set of a given name and type ‘MX’ from a DNS zone.|
|/dnszones/MX/read|Get the record set of type ‘MX’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag.|
|/dnszones/MX/write|Create or update a record set of type ‘MX’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/NS/delete|Deletes the DNS record set of type NS|
|/dnszones/NS/read|Gets DNS record set of type NS|
|/dnszones/NS/write|Creates or updates DNS record set of type NS|
|/dnszones/providers/Microsoft.Insights/diagnosticSettings/read|Gets the DNS zone diagnostic settings|
|/dnszones/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the DNS zone diagnostic settings|
|/dnszones/providers/Microsoft.Insights/metricDefinitions/read|Gets the DNS zone metric definitions|
|/dnszones/PTR/delete|Remove the record set of a given name and type ‘PTR’ from a DNS zone.|
|/dnszones/PTR/read|Get the record set of type ‘PTR’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag.|
|/dnszones/PTR/write|Create or update a record set of type ‘PTR’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/read|Get the DNS zone, in JSON format. The zone properties include tags, etag, numberOfRecordSets, and maxNumberOfRecordSets. Note that this command does not retrieve the record sets contained within the zone.|
|/dnszones/recordsets/read|Gets DNS record sets across types|
|/dnszones/SOA/read|Gets DNS record set of type SOA|
|/dnszones/SOA/write|Creates or updates DNS record set of type SOA|
|/dnszones/SRV/delete|Remove the record set of a given name and type ‘SRV’ from a DNS zone.|
|/dnszones/SRV/read|Get the record set of type ‘SRV’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag.|
|/dnszones/SRV/write|Create or update record set of type SRV|
|/dnszones/TXT/delete|Remove the record set of a given name and type ‘TXT’ from a DNS zone.|
|/dnszones/TXT/read|Get the record set of type ‘TXT’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag.|
|/dnszones/TXT/write|Create or update a record set of type ‘TXT’ within a DNS zone. The records specified will replace the current records in the record set.|
|/dnszones/write|Create or update a DNS zone within a resource group.  Used to update the tags on a DNS zone resource. Note that this command can not be used to create or update record sets within the zone.|
|/expressRouteCircuits/authorizations/delete|Deletes an ExpressRouteCircuit Authorization|
|/expressRouteCircuits/authorizations/read|Gets an ExpressRouteCircuit Authorization|
|/expressRouteCircuits/authorizations/write|Creates or updates an existing ExpressRouteCircuit Authorization|
|/expressRouteCircuits/delete|Deletes an ExpressRouteCircuit|
|/expressRouteCircuits/peerings/arpTables/action|Gets an ExpressRouteCircuit Peering ArpTable|
|/expressRouteCircuits/peerings/connections/delete|Deletes an ExpressRouteCircuit Connection|
|/expressRouteCircuits/peerings/connections/read|Gets an ExpressRouteCircuit Connection|
|/expressRouteCircuits/peerings/connections/write|Creates or updates an existing ExpressRouteCircuit Connection Resource|
|/expressRouteCircuits/peerings/delete|Deletes an ExpressRouteCircuit Peering|
|/expressRouteCircuits/peerings/read|Gets an ExpressRouteCircuit Peering|
|/expressRouteCircuits/peerings/routeTables/action|Gets an ExpressRouteCircuit Peering RouteTable|
|/expressRouteCircuits/peerings/routeTablesSummary/action|Gets an ExpressRouteCircuit Peering RouteTable Summary|
|/expressRouteCircuits/peerings/stats/read|Gets an ExpressRouteCircuit Peering Stat|
|/expressRouteCircuits/peerings/write|Creates or updates an existing ExpressRouteCircuit Peering|
|/expressRouteCircuits/providers/Microsoft.Insights/diagnosticSettings/read|Gets diagnostic settings for ExpressRoute Circuits|
|/expressRouteCircuits/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates diagnostic settings for ExpressRoute Circuits|
|/expressRouteCircuits/providers/Microsoft.Insights/logDefinitions/read|Get the events for ExpressRoute Circuits|
|/expressRouteCircuits/providers/Microsoft.Insights/metricDefinitions/read|Gets the metric definitions for ExpressRoute Circuits|
|/expressRouteCircuits/read|Get an ExpressRouteCircuit|
|/expressRouteCircuits/stats/read|Gets an ExpressRouteCircuit Stat|
|/expressRouteCircuits/write|Creates or updates an existing ExpressRouteCircuit|
|/expressRouteCrossConnections/delete|Delete Express Route Cross Connection|
|/expressRouteCrossConnections/join/action|Joins an Express Route Cross Connection|
|/expressRouteCrossConnections/peerings/arpTables/action|Gets an Express Route Cross Connection Peering Arp Table|
|/expressRouteCrossConnections/peerings/delete|Deletes an Express Route Cross Connection Peering|
|/expressRouteCrossConnections/peerings/read|Gets an Express Route Cross Connection Peering|
|/expressRouteCrossConnections/peerings/routeTables/action|Gets an Express Route Cross Connection Peering Route Table|
|/expressRouteCrossConnections/peerings/routeTableSummary/action|Gets an Express Route Cross Connection Peering Route Table Summary|
|/expressRouteCrossConnections/peerings/stats/read|Gets an Express Route Cross Connection Peering Stat|
|/expressRouteCrossConnections/peerings/write|Creates an Express Route Cross Connection Peering or Updates an existing Express Route Cross Connection Peering|
|/expressRouteCrossConnections/read|Get Express Route Cross Connection|
|/expressRouteCrossConnections/write|Create or Update Express Route Cross Connection|
|/expressRouteServiceProviders/read|Gets Express Route Service Providers|
|/loadBalancers/backendAddressPools/join/action|Joins a load balancer backend address pool|
|/loadBalancers/backendAddressPools/read|Gets a load balancer backend address pool definition|
|/loadBalancers/delete|Deletes a load balancer|
|/loadBalancers/frontendIPConfigurations/read|Gets a load balancer frontend IP configuration definition|
|/loadBalancers/inboundNatPools/join/action|Joins a load balancer inbound nat pool|
|/loadBalancers/inboundNatPools/read|Gets a load balancer inbound nat pool definition|
|/loadBalancers/inboundNatRules/delete|Deletes a load balancer inbound nat rule|
|/loadBalancers/inboundNatRules/join/action|Joins a load balancer inbound nat rule|
|/loadBalancers/inboundNatRules/read|Gets a load balancer inbound nat rule definition|
|/loadBalancers/inboundNatRules/write|Creates a load balancer inbound nat rule or updates an existing load balancer inbound nat rule|
|/loadBalancers/loadBalancingRules/read|Gets a load balancer load balancing rule definition|
|/loadBalancers/networkInterfaces/read|Gets references to all the network interfaces under a load balancer|
|/loadBalancers/outboundNatRules/read|Gets a load balancer outbound nat rule definition|
|/loadBalancers/probes/join/action|Allows using probes of a load balancer. For example, with this permission healthProbe property of VM scale set can reference the probe.|
|/loadBalancers/probes/read|Gets a load balancer probe|
|/loadBalancers/providers/Microsoft.Insights/diagnosticSettings/read|Gets the Load Balancer Diagnostic Settings|
|/loadBalancers/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the Load Balancer Diagnostic Settings|
|/loadBalancers/providers/Microsoft.Insights/logDefinitions/read|Gets the events for Load Balancer|
|/loadBalancers/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Load Balancer|
|/loadBalancers/read|Gets a load balancer definition|
|/loadBalancers/virtualMachines/read|Gets references to all the virtual machines under a load balancer|
|/loadBalancers/write|Creates a load balancer or updates an existing load balancer|
|/localnetworkgateways/delete|Deletes LocalNetworkGateway|
|/localnetworkgateways/read|Gets LocalNetworkGateway|
|/localnetworkgateways/write|Creates or updates an existing LocalNetworkGateway|
|/locations/checkDnsNameAvailability/read|Checks if dns label is available at the specified location|
|/locations/operationResults/read|Gets operation result of an async POST or DELETE operation|
|/locations/operations/read|Gets operation resource that represents status of an asynchronous operation|
|/locations/usages/read|Gets the resources usage metrics|
|/locations/virtualNetworkAvailableEndpointServices/read|Gets a list of available Virtual Network Endpoint Services|
|/networkInterfaces/delete|Deletes a network interface|
|/networkInterfaces/diagnosticIdentity/read|Gets Diagnostic Identity Of The Resource|
|/networkInterfaces/effectiveNetworkSecurityGroups/action|Get Network Security Groups configured On Network Interface Of The Vm|
|/networkInterfaces/effectiveRouteTable/action|Get Route Table configured On Network Interface Of The Vm|
|/networkInterfaces/ipconfigurations/read|Gets a network interface ip configuration definition. |
|/networkInterfaces/join/action|Joins a Virtual Machine to a network interface|
|/networkInterfaces/loadBalancers/read|Gets all the load balancers that the network interface is part of|
|/networkInterfaces/providers/Microsoft.Insights/metricDefinitions/read|Gets available metrics for the Network Interface|
|/networkInterfaces/read|Gets a network interface definition. |
|/networkInterfaces/write|Creates a network interface or updates an existing network interface. |
|/networkSecurityGroups/defaultSecurityRules/read|Gets a default security rule definition|
|/networkSecurityGroups/delete|Deletes a network security group|
|/networkSecurityGroups/join/action|Joins a network security group|
|/networksecuritygroups/providers/Microsoft.Insights/diagnosticSettings/read|Gets the Network Security Groups Diagnostic Settings|
|/networksecuritygroups/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the Network Security Groups diagnostic settings, this operation is supplimented by insghts resource provider.|
|/networksecuritygroups/providers/Microsoft.Insights/logDefinitions/read|Gets the events for network security group|
|/networkSecurityGroups/read|Gets a network security group definition|
|/networkSecurityGroups/securityRules/delete|Deletes a security rule|
|/networkSecurityGroups/securityRules/read|Gets a security rule definition|
|/networkSecurityGroups/securityRules/write|Creates a security rule or updates an existing security rule|
|/networkSecurityGroups/write|Creates a network security group or updates an existing network security group|
|/networkWatchers/availableProvidersList/action|Returns all available internet service providers for a specified Azure region.|
|/networkWatchers/azureReachabilityReport/action|Returns the relative latency score for internet service providers from a specified location to Azure regions.|
|/networkWatchers/configureFlowLog/action|Configures flow logging for a target resource.|
|/networkWatchers/connectionMonitors/delete|Deletes a Connection Monitor|
|/networkWatchers/connectionMonitors/providers/Microsoft.Insights/ diagnosticSettings/read|Get the diagnostic settings of Connection Monitor|
|/networkWatchers/connectionMonitors/providers/Microsoft.Insights/ diagnosticSettings/write|Creates or updates the Connection Monitor Diagnostic Settings|
|/networkWatchers/connectionMonitors/providers/Microsoft.Insights/ metricDefinitions/read|Gets the available metrics for Connection Monitor|
|/networkWatchers/connectionMonitors/query/action|Query monitoring connectivity between specified endpoints|
|/networkWatchers/connectionMonitors/read|Get Connection Monitor details|
|/networkWatchers/connectionMonitors/start/action|Start monitoring connectivity between specified endpoints|
|/networkWatchers/connectionMonitors/stop/action|Stop/pause monitoring connectivity between specified endpoints|
|/networkWatchers/connectionMonitors/write|Creates a Connection Monitor|
|/networkWatchers/connectivityCheck/action|Verifies the possibility of establishing a direct TCP connection from a virtual machine to a given endpoint including another VM or an arbitrary remote server.|
|/networkWatchers/delete|Deletes a network watcher|
|/networkWatchers/ipFlowVerify/action|Returns whether the packet is allowed or denied to or from a particular destination.|
|/networkWatchers/lenses/delete|Deletes a Lens|
|/networkWatchers/lenses/query/action|Query monitoring network traffic on a specified endpoint|
|/networkWatchers/lenses/read|Get Lens details|
|/networkWatchers/lenses/start/action|Start monitoring network traffic on a specified endpoint|
|/networkWatchers/lenses/stop/action|Stop/pause monitoring network traffic on a specified endpoint|
|/networkWatchers/lenses/write|Creates a Lens|
|/networkWatchers/nextHop/action|For a specified target and destination IP address, return the next hop type and next hope IP address.|
|/networkWatchers/packetCaptures/delete|Deletes a packet capture|
|/networkWatchers/packetCaptures/queryStatus/action|Gets information about properties and status of a packet capture resource.|
|/networkWatchers/packetCaptures/read|Get the packet capture definition|
|/networkWatchers/packetCaptures/stop/action|Stop the running packet capture session.|
|/networkWatchers/packetCaptures/write|Creates a packet capture|
|/networkWatchers/queryFlowLogStatus/action|Gets the status of flow logging on a resource.|
|/networkWatchers/queryTroubleshootResult/action|Gets the troubleshooting result from the previously run or currently running troubleshooting operation.|
|/networkWatchers/read|Get the network watcher definition|
|/networkWatchers/securityGroupView/action|View the configured and effective network security group rules applied on a VM.|
|/networkWatchers/topology/action|Gets a network level view of resources and their relationships in a resource group.|
|/networkWatchers/troubleshoot/action|Starts troubleshooting on a Networking resource in Azure.|
|/networkWatchers/write|Creates a network watcher or updates an existing network watcher|
|/operations/read|Get Available Operations|
|/publicIPAddresses/delete|Deletes a public Ip address.|
|/publicIPAddresses/join/action|Joins a public ip address|
|/publicIPAddresses/providers/Microsoft.Insights/diagnosticSettings/read|Get the diagnostic settings of Public IP Address|
|/publicIPAddresses/providers/Microsoft.Insights/diagnosticSettings/write|Create or update the diagnostic settings of Public IP Address|
|/publicIPAddresses/providers/Microsoft.Insights/logDefinitions/read|Get the log definitions of Public IP Address|
|/publicIPAddresses/providers/Microsoft.Insights/metricDefinitions/read|Get the metrics definitions of Public IP Address|
|/publicIPAddresses/read|Gets a public ip address definition.|
|/publicIPAddresses/write|Creates a public Ip address or updates an existing public Ip address. |
|/register/action|Registers the subscription|
|/routeFilters/delete|Deletes a route filter definition|
|/routeFilters/join/action|Joins a route filter|
|/routeFilters/read|Gets a route filter definition|
|/routeFilters/routeFilterRules/delete|Deletes a route filter rule definition|
|/routeFilters/routeFilterRules/read|Gets a route filter rule definition|
|/routeFilters/routeFilterRules/write|Creates a route filter rule or Updates an existing route filter rule|
|/routeFilters/write|Creates a route filter or Updates an existing rotue filter|
|/routeTables/delete|Deletes a route table definition|
|/routeTables/join/action|Joins a route table|
|/routeTables/read|Gets a route table definition|
|/routeTables/routes/delete|Deletes a route definition|
|/routeTables/routes/read|Gets a route definition|
|/routeTables/routes/write|Creates a route or Updates an existing route|
|/routeTables/write|Creates a route table or Updates an existing rotue table|
|/securegateways/applicationRuleCollections/delete|Deletes an Application Rule Collection for a Secure Gateway|
|/securegateways/applicationRuleCollections/read|Retrieve an Application Rule Collection for a given Secure Gateway|
|/securegateways/applicationRuleCollections/write|Creates or updates an Application Rule Collection for a Secure Gateway|
|/securegateways/delete|Delete Secure Gateway|
|/securegateways/networkRuleCollections/delete|Deletes a Network Rule Collection for a Secure Gateway|
|/securegateways/networkRuleCollections/read|Retrieve a Network Rule Collection for a given Secure Gateway|
|/securegateways/networkRuleCollections/write|Creates or updates a Network Rule Collection for a Secure Gateway|
|/securegateways/read|Get Secure Gateway|
|/securegateways/write|Creates or updates a Secure Gateway|
|/serviceEndpointPolicies/delete|Deletes a Service Endpoint Policy|
|/serviceEndpointPolicies/join/action|Joins a Service Endpoint Policy|
|/serviceEndpointPolicies/joinSubnet/action|Joins a Subnet To Service Endpoint Policies|
|/serviceEndpointPolicies/read|Gets a Service Endpoint Policy Description|
|/serviceEndpointPolicies/serviceEndpointPolicyDefinitions/delete|Deletes a Service Endpoint Policy Definition|
|/serviceEndpointPolicies/serviceEndpointPolicyDefinitions/read|Gets a Service Endpoint Policy Definition Decription|
|/serviceEndpointPolicies/serviceEndpointPolicyDefinitions/write|Creates a Service Endpoint Policy Definition or updates an existing Service Endpoint Policy Definition|
|/serviceEndpointPolicies/write|Creates a Service Endpoint Policy or updates an existing Service Endpoint Policy|
|/trafficManagerGeographicHierarchies/read|Gets the Traffic Manager Geographic Hierarchy containing regions which can be used with the Geographic traffic routing method|
|/trafficManagerProfiles/azureEndpoints/delete|Deletes an Azure Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted Azure Endpoint.|
|/trafficManagerProfiles/azureEndpoints/read|Gets an Azure Endpoint which belongs to a Traffic Manager Profile, including all the properties of that Azure Endpoint.|
|/trafficManagerProfiles/azureEndpoints/write|Add a new Azure Endpoint in an existing Traffic Manager Profile or update the properties of an existing Azure Endpoint in that Traffic Manager Profile.|
|/trafficManagerProfiles/delete|Delete the Traffic Manager profile. All settings associated with the Traffic Manager profile will be lost, and the profile can no longer be used to route traffic.|
|/trafficManagerProfiles/externalEndpoints/delete|Deletes an External Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted External Endpoint.|
|/trafficManagerProfiles/externalEndpoints/read|Gets an External Endpoint which belongs to a Traffic Manager Profile, including all the properties of that External Endpoint.|
|/trafficManagerProfiles/externalEndpoints/write|Add a new External Endpoint in an existing Traffic Manager Profile or update the properties of an existing External Endpoint in that Traffic Manager Profile.|
|/trafficManagerProfiles/heatMaps/read|Gets the Traffic Manager Heat Map for the given Traffic Manager profile which contains query counts and latency data by location and source IP.|
|/trafficManagerProfiles/nestedEndpoints/delete|Deletes an Nested Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted Nested Endpoint.|
|/trafficManagerProfiles/nestedEndpoints/read|Gets an Nested Endpoint which belongs to a Traffic Manager Profile, including all the properties of that Nested Endpoint.|
|/trafficManagerProfiles/nestedEndpoints/write|Add a new Nested Endpoint in an existing Traffic Manager Profile or update the properties of an existing Nested Endpoint in that Traffic Manager Profile.|
|/trafficManagerProfiles/providers/Microsoft.Insights/diagnosticSettings/read|Gets the Traffic Manager Diagnostic Settings|
|/trafficManagerProfiles/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the Traffic Manager diagnostic settings, this operation is supplimented by insights resource provider.|
|/trafficManagerProfiles/providers/Microsoft.Insights/logDefinitions/read|Gets the events for Traffic Manager|
|/trafficManagerProfiles/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Traffic Manager.|
|/trafficManagerProfiles/read|Get the Traffic Manager profile configuration. This includes DNS settings, traffic routing settings, endpoint monitoring settings, and the list of endpoints routed by this Traffic Manager profile.|
|/trafficManagerProfiles/write|Create a Traffic Manager profile, or modify the configuration of an existing Traffic Manager profile. This includes enabling or disabling a profile and modifying DNS settings, traffic routing settings, or endpoint monitoring settings. Endpoints routed by the Traffic Manager profile can be added, removed, enabled or disabled.|
|/trafficManagerUserMetricsKeys/delete|Deletes the subscription-level key used for Realtime User Metrics collection.|
|/trafficManagerUserMetricsKeys/read|Gets the subscription-level key used for Realtime User Metrics collection.|
|/trafficManagerUserMetricsKeys/write|Creates a new subscription-level key to be used for Realtime User Metrics collection.|
|/unregister/action|Unregisters the subscription|
|/virtualHubs/delete|Deletes a Virtual Hub|
|/virtualHubs/hubVirtualNetworkConnections/delete|Deletes a HubVirtualNetworkConnection|
|/virtualHubs/hubVirtualNetworkConnections/read|Get a HubVirtualNetworkConnection|
|/virtualHubs/hubVirtualNetworkConnections/write|Create or update a HubVirtualNetworkConnection|
|/virtualHubs/read|Get a Virtual Hub|
|/virtualHubs/write|Create or update a Virtual Hub|
|/virtualnetworkgateways/connections/read|Get VirtualNetworkGatewayConnection|
|/virtualNetworkGateways/delete|Deletes a virtualNetworkGateway|
|/virtualnetworkgateways/generatevpnclientpackage/action|Generate VpnClient package for virtualNetworkGateway|
|/virtualnetworkgateways/generatevpnprofile/action|Generate VpnProfile package for VirtualNetworkGateway|
|/virtualnetworkgateways/getadvertisedroutes/action|Gets virtualNetworkGateway advertised routes|
|/virtualnetworkgateways/getbgppeerstatus/action|Gets virtualNetworkGateway bgp peer status|
|/virtualnetworkgateways/getlearnedroutes/action|Gets virtualnetworkgateway learned routes|
|/virtualnetworkgateways/getvpnclientipsecparameters/action|Get Vpnclient Ipsec parameters for VirtualNetworkGateway P2S client.|
|/virtualnetworkgateways/getvpnprofilepackageurl/action|Gets the URL of a pre-generated vpn client profile package|
|/virtualNetworkGateways/providers/Microsoft.Insights/diagnosticSettings/read|Gets the Virtual Network Gateway Diagnostic Settings|
|/virtualNetworkGateways/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the Virtual Network Gateway diagnostic settings, this operation is supplimented by insights resource provider.|
|/virtualNetworkGateways/providers/Microsoft.Insights/logDefinitions/read|Gets the events for Virtual Network Gateway|
|/virtualNetworkGateways/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Virtual Network Gateway|
|/virtualNetworkGateways/read|Gets a VirtualNetworkGateway|
|/virtualnetworkgateways/reset/action|Resets a virtualNetworkGateway|
|/virtualnetworkgateways/setvpnclientipsecparameters/action|Set Vpnclient Ipsec parameters for VirtualNetworkGateway P2S client.|
|/virtualnetworkgateways/supportedvpndevices/action|Lists Supported Vpn Devices|
|/virtualNetworkGateways/write|Creates or updates a VirtualNetworkGateway|
|/virtualNetworks/checkIpAddressAvailability/read|Check if Ip Address is available at the specified virtual network|
|/virtualNetworks/customViews/get/action|Get a Virtual Network custom view content|
|/virtualNetworks/customViews/read|Get definition of a custom view of Virtual Network|
|/virtualNetworks/delete|Deletes a virtual network|
|/virtualNetworks/peer/action|Peers a virtual network with another virtual network|
|/virtualNetworks/providers/Microsoft.Insights/diagnosticSettings/read|Get the diagnostic settings of Virtual Network|
|/virtualNetworks/providers/Microsoft.Insights/diagnosticSettings/write|Create or update the diagnostic settings of the Virtual Network|
|/virtualNetworks/providers/Microsoft.Insights/logDefinitions/read|Get the log definitions of Virtual Network|
|/virtualNetworks/providers/Microsoft.Insights/metricDefinitions/read|Get the metric definitions of Virtual Network|
|/virtualNetworks/read|Get the virtual network definition|
|/virtualNetworks/remoteVirtualNetworkPeeringProxies/delete|Deletes a virtual network peering proxy|
|/virtualNetworks/remoteVirtualNetworkPeeringProxies/read|Gets a virtual network peering proxy definition|
|/virtualNetworks/remoteVirtualNetworkPeeringProxies/write|Creates a virtual network peering proxy or updates an existing virtual network peering proxy|
|/virtualNetworks/subnets/delete|Deletes a virtual network subnet|
|/virtualNetworks/subnets/join/action|Joins a virtual network|
|/virtualNetworks/subnets/joinViaServiceEndpoint/action|Joins resource such as storage account or SQL database to a subnet.|
|/virtualNetworks/subnets/read|Gets a virtual network subnet definition|
|/virtualNetworks/subnets/resourceNavigationLinks/delete|Deletes a Resource Navigation Link|
|/virtualNetworks/subnets/resourceNavigationLinks/read|Get the Resource Navigation Link definition|
|/virtualNetworks/subnets/resourceNavigationLinks/write|Creates a Resource Navigation Link or updates an existing Resource Navigation Link|
|/virtualNetworks/subnets/virtualMachines/read|Gets references to all the virtual machines in a virtual network subnet|
|/virtualNetworks/subnets/write|Creates a virtual network subnet or updates an existing virtual network subnet|
|/virtualNetworks/taggedTrafficConsumers/delete|Deletes a Tagged Traffic Consumer|
|/virtualNetworks/taggedTrafficConsumers/read|Get the Tagged Traffic Consumer definition|
|/virtualNetworks/taggedTrafficConsumers/validate/action|Validates a Tagged Traffic Consumer|
|/virtualNetworks/taggedTrafficConsumers/write|Creates a Tagged Traffic Consumer or updates an existing Tagged Traffic Consumer|
|/virtualNetworks/usages/read|Get the IP usages for each subnet of the virtual network|
|/virtualNetworks/virtualMachines/read|Gets references to all the virtual machines in a virtual network|
|/virtualNetworks/virtualNetworkPeerings/delete|Deletes a virtual network peering|
|/virtualNetworks/virtualNetworkPeerings/read|Gets a virtual network peering definition|
|/virtualNetworks/virtualNetworkPeerings/write|Creates a virtual network peering or updates an existing virtual network peering|
|/virtualNetworks/write|Creates a virtual network or updates an existing virtual network|
|/virtualNetworkTaps/delete|Delete Virtual Network Tap|
|/virtualNetworkTaps/join/action|Joins a virtual network tap|
|/virtualNetworkTaps/read|Get Virtual Network Tap|
|/virtualNetworkTaps/write|Create or Update Virtual Network Tap|
|/virtualwans/delete|Deletes a Virtual Wan|
|/virtualwans/read|Get a Virtual Wan|
|/virtualWans/virtualHubProxies/delete|Deletes a Virtual Hub proxy|
|/virtualWans/virtualHubProxies/read|Gets a Virtual Hub proxy definition|
|/virtualWans/virtualHubProxies/write|Creates a Virtual Hub proxy or updates a Virtual Hub proxy|
|/virtualwans/virtualHubs/read|Gets all Virtual Hubs that are associated to a Virtual Wan.|
|/virtualwans/vpnconfiguration/read|Gets a Vpn Configuration|
|/virtualWans/vpnSiteProxies/delete|Deletes a Vpn Site proxy|
|/virtualWans/vpnSiteProxies/read|Gets a Vpn Site proxy definition|
|/virtualWans/vpnSiteProxies/write|Creates a Vpn Site proxy or updates a Vpn Site proxy|
|/virtualwans/vpnSites/read|Gets all VPN Sites that are associated to a Virtual Wan.|
|/virtualwans/write|Create or update a Virtual Wan|
|/vpnGateways/read|Gets a VpnGateway.|
|/vpnGateways/vpnConnections/read|Gets a VpnConnection.|
|/vpnGateways/vpnConnections/write|Puts a VpnConnection.|
|/vpnGateways/write|Puts a VpnGateway.|
|/vpnsites/delete|Deletes a Vpn Site resource.|
|/vpnsites/read|Gets a Vpn Site resource.|
|/vpnsites/write|Creates or updates a Vpn Site resource.|

## <a name="microsoftnotificationhubs"></a>Microsoft.NotificationHubs

| Operation | Description |
|---|---|
|/CheckNamespaceAvailability/action|Checks whether or not a given Namespace resource name is available within the NotificationHub service.|
|/Namespaces/authorizationRules/action|Get the list of Namespaces Authorization Rules description.|
|/Namespaces/authorizationRules/delete|Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted. |
|/Namespaces/authorizationRules/listkeys/action|Get the Connection String to the Namespace|
|/Namespaces/authorizationRules/read|Get the list of Namespaces Authorization Rules description.|
|/Namespaces/authorizationRules/regenerateKeys/action|Namespace Authorization Rule Regenerate Primary/SecondaryKey, Specify the Key that needs to be regenerated|
|/Namespaces/authorizationRules/write|Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated.|
|/Namespaces/CheckNotificationHubAvailability/action|Checks whether or not a given NotificationHub name is available inside a Namespace.|
|/Namespaces/Delete|Delete Namespace Resource|
|/Namespaces/NotificationHubs/authorizationRules/action|Get the list of Notification Hub Authorization Rules|
|/Namespaces/NotificationHubs/authorizationRules/delete|Delete Notification Hub Authorization Rules|
|/Namespaces/NotificationHubs/authorizationRules/listkeys/action|Get the Connection String to the Notification Hub|
|/Namespaces/NotificationHubs/authorizationRules/read|Get the list of Notification Hub Authorization Rules|
|/Namespaces/NotificationHubs/authorizationRules/regenerateKeys/action|Notification Hub Authorization Rule Regenerate Primary/SecondaryKey, Specify the Key that needs to be regenerated|
|/Namespaces/NotificationHubs/authorizationRules/write|Create Notification Hub Authorization Rules and Update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated.|
|/Namespaces/NotificationHubs/debugSend/action|Send a test push notification.|
|/Namespaces/NotificationHubs/Delete|Delete Notification Hub Resource|
|/Namespaces/NotificationHubs/metricDefinitions/read|Get list of Namespace metrics Resource Descriptions|
|/Namespaces/NotificationHubs/pnsCredentials/action|Get All Notification Hub PNS Credentials. This includes, WNS, MPNS, APNS, GCM and Baidu credentials|
|/Namespaces/NotificationHubs/read|Get list of Notification Hub Resource Descriptions|
|/Namespaces/NotificationHubs/write|Create a Notification Hub and Update its properties. Its properties mainly include PNS Credentials. Authorization Rules and TTL|
|/Namespaces/read|Get the list of Namespace Resource Description|
|/Namespaces/write|Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated.|
|/register/action|Registers the subscription for the NotifciationHubs resource provider and enables the creation of Namespaces and NotificationHubs|

## <a name="microsoftoperationalinsights"></a>Microsoft.OperationalInsights

| Operation | Description |
|---|---|
|/linkTargets/read|Lists existing accounts that are not associated with an Azure subscription. To link this Azure subscription to a workspace, use a customer id returned by this operation in the customer id property of the Create Workspace operation.|
|/register/action|Register a subscription to a resource provider.|
|/workspaces/analytics/query/action|Search using new engine.|
|/workspaces/analytics/query/schema/read|Get search schema V2.|
|/workspaces/api/query/action|Search using new engine.|
|/workspaces/api/query/schema/read|Get search schema V2.|
|/workspaces/configurationScopes/delete|Delete Configuration Scope|
|/workspaces/configurationScopes/read|Get Configuration Scope|
|/workspaces/configurationScopes/write|Set Configuration Scope|
|/workspaces/datasources/delete|Delete datasources under a workspace.|
|/workspaces/datasources/read|Get datasources under a workspace.|
|/workspaces/datasources/write|Create/Update datasources under a workspace.|
|/workspaces/delete|Deletes a workspace. If the workspace was linked to an existing workspace at creation time then the workspace it was linked to is not deleted.|
|/workspaces/generateregistrationcertificate/action|Generates Registration Certificate for the workspace. This Certificate is used to connect Microsoft System Center Operation Manager to the workspace.|
|/workspaces/intelligencepacks/disable/action|Disables an intelligence pack for a given workspace.|
|/workspaces/intelligencepacks/enable/action|Enables an intelligence pack for a given workspace.|
|/workspaces/intelligencepacks/read|Lists all intelligence packs that are visible for a given worksapce and also lists whether the pack is enabled or disabled for that workspace.|
|/workspaces/linkedServices/delete|Delete linked services under given workspace.|
|/workspaces/linkedServices/read|Get linked services under given workspace.|
|/workspaces/linkedServices/write|Create/Update linked services under given workspace.|
|/workspaces/listKeys/action|Retrieves the list keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace.|
|/workspaces/listKeys/read|Retrieves the list keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace.|
|/workspaces/managementGroups/read|Gets the names and metadata for System Center Operations Manager management groups connected to this workspace.|
|/workspaces/metricDefinitions/read|Get Metric Definitions under workspace|
|/workspaces/notificationSettings/delete|Delete the user's notification settings for the workspace.|
|/workspaces/notificationSettings/read|Get the user's notification settings for the workspace.|
|/workspaces/notificationSettings/write|Set the user's notification settings for the workspace.|
|/workspaces/purge/action|Delete specified data from workspace|
|/workspaces/read|Gets an existing workspace|
|/workspaces/savedSearches/delete|Deletes a saved search query|
|/workspaces/savedSearches/read|Gets a saved search query|
|/workspaces/savedSearches/write|Creates a saved search query|
|/workspaces/schema/read|Gets the search schema for the workspace.  Search schema includes the exposed fields and their types.|
|/workspaces/search/action|Executes a search query|
|/workspaces/sharedKeys/action|Retrieves the shared keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace.|
|/workspaces/sharedKeys/read|Retrieves the shared keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace.|
|/workspaces/storageinsightconfigs/delete|Deletes a storage configuration. This will stop Microsoft Operational Insights from reading data from the storage account.|
|/workspaces/storageinsightconfigs/read|Gets a storage configuration.|
|/workspaces/storageinsightconfigs/write|Creates a new storage configuration. These configurations are used to pull data from a location in an existing storage account.|
|/workspaces/usages/read|Gets usage data for a workspace including the amount of data read by the workspace.|
|/workspaces/write|Creates a new workspace or links to an existing workspace by providing the customer id from the existing workspace.|

## <a name="microsoftoperationsmanagement"></a>Microsoft.OperationsManagement

| Operation | Description |
|---|---|
|/managementAssociations/delete|Delete existing Management Association|
|/managementAssociations/read|Get Existing Management Association|
|/managementAssociations/write|Create a new Management Association|
|/managementConfigurations/delete|Delete existing Management Configuratin|
|/managementConfigurations/read|Get Existing Management Configuration|
|/managementConfigurations/write|Create a new Management Configuration|
|/register/action|Register a subscription to a resource provider.|
|/solutions/delete|Delete existing OMS solution|
|/solutions/read|Get exiting OMS solution|
|/solutions/write|Create new OMS solution|

## <a name="microsoftportal"></a>Microsoft.Portal

| Operation | Description |
|---|---|
|/dashboards/delete|Removes the dashboard from the subscription.|
|/dashboards/read|Reads the dashboards for the subscription.|
|/dashboards/write|Add or modify dashboard to a subscription.|

## <a name="microsoftpowerbidedicated"></a>Microsoft.PowerBIDedicated

| Operation | Description |
|---|---|
|/capacities/checkNameAvailability/action|Checks that given Power BI Dedicated Capacity name is valid and not in use.|
|/capacities/delete|Deletes the Power BI Dedicated Capacity.|
|/capacities/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Power BI Dedicated Capacity.|
|/capacities/read|Retrieves the information of the specified Power BI Dedicated Capacity.|
|/capacities/write|Creates or updates the specified Power BI Dedicated Capacity.|

## <a name="microsoftrecoveryservices"></a>Microsoft.RecoveryServices

| Operation | Description |
|---|---|
|/locations/allocatedStamp/read|GetAllocatedStamp is internal operation used by service|
|/locations/allocateStamp/action|AllocateStamp is internal operation used by service|
|/locations/backupPreValidateProtection/action||
|/locations/backupStatus/action|Check Backup Status for Recovery Services Vaults|
|/locations/backupValidateFeatures/action|Validate Features|
|/operations/read|Operation returns the list of Operations for a Resource Provider|
|/register/action|Registers subscription for given Resource Provider|
|/Vaults/backupconfig/read|Returns Configuration for Recovery Services Vault.|
|/Vaults/backupconfig/write|Updates Configuration for Recovery Services Vault.|
|/Vaults/backupEngines/read|Returns all the backup management servers registered with vault.|
|/Vaults/backupFabrics/{fabricName}/protectionContainers/{containerName}/items/read|Get all items in a container|
|/Vaults/backupFabrics/backupProtectionIntent/write|Create a backup Protection Intent|
|/Vaults/backupFabrics/operationResults/read|Returns status of the operation|
|/Vaults/backupFabrics/protectableContainers/read|Get all protectable containers|
|/Vaults/backupFabrics/protectionContainers/inquire/action|Do inquiry for workloads within a container|
|/Vaults/backupFabrics/protectionContainers/operationResults/read|Gets result of Operation performed on Protection Container.|
|/Vaults/backupFabrics/protectionContainers/protectedItems/backup/action|Performs Backup for Protected Item.|
|/Vaults/backupFabrics/protectionContainers/protectedItems/delete|Deletes Protected Item|
|/Vaults/backupFabrics/protectionContainers/protectedItems/operationResults/read|Gets Result of Operation Performed on Protected Items.|
|/Vaults/backupFabrics/protectionContainers/protectedItems/operationsStatus/read|Returns the status of Operation performed on Protected Items.|
|/Vaults/backupFabrics/protectionContainers/protectedItems/read|Returns object details of the Protected Item|
|/Vaults/backupFabrics/protectionContainers/protectedItems/ recoveryPoints/provisionInstantItemRecovery/action|Provision Instant Item Recovery for Protected Item|
|/Vaults/backupFabrics/protectionContainers/protectedItems/recoveryPoints/read|Get Recovery Points for Protected Items.|
|/Vaults/backupFabrics/protectionContainers/protectedItems/ recoveryPoints/restore/action|Restore Recovery Points for Protected Items.|
|/Vaults/backupFabrics/protectionContainers/protectedItems/ recoveryPoints/revokeInstantItemRecovery/action|Revoke Instant Item Recovery for Protected Item|
|/Vaults/backupFabrics/protectionContainers/protectedItems/write|Create a backup Protected Item|
|/Vaults/backupFabrics/protectionContainers/read|Returns all registered containers|
|/Vaults/backupFabrics/protectionContainers/write|Creates a registered container|
|/Vaults/backupFabrics/refreshContainers/action|Refreshes the container list|
|/Vaults/backupJobs/cancel/action|Cancel the Job|
|/Vaults/backupJobs/operationResults/read|Returns the Result of Job Operation.|
|/Vaults/backupJobs/read|Returns all Job Objects|
|/Vaults/backupJobsExport/action|Export Jobs|
|/Vaults/backupJobsExport/operationResults/read|Returns the Result of Export Job Operation.|
|/Vaults/backupManagementMetaData/read|Returns Backup Management Metadata for Recovery Services Vault.|
|/Vaults/backupOperationResults/read|Returns Backup Operation Result for Recovery Services Vault.|
|/Vaults/backupOperations/read|Returns Backup Operation Status for Recovery Services Vault.|
|/Vaults/backupPolicies/delete|Delete a Protection Policy|
|/Vaults/backupPolicies/operationResults/read|Get Results of Policy Operation.|
|/Vaults/backupPolicies/operations/read|Get Status of Policy Operation.|
|/Vaults/backupPolicies/read|Returns all Protection Policies|
|/Vaults/backupPolicies/write|Creates Protection Policy|
|/Vaults/backupProtectableItems/read|Returns list of all Protectable Items.|
|/Vaults/backupProtectedItems/read|Returns the list of all Protected Items.|
|/Vaults/backupProtectionContainers/read|Returns all containers belonging to the subscription|
|/Vaults/backupSecurityPIN/action|Returns Security PIN Information for Recovery Services Vault.|
|/Vaults/backupstorageconfig/read|Returns Storage Configuration for Recovery Services Vault.|
|/Vaults/backupstorageconfig/write|Updates Storage Configuration for Recovery Services Vault.|
|/Vaults/backupUsageSummaries/read|Returns summaries for Protected Items and Protected Servers for a Recovery Services .|
|/Vaults/certificates/write|The Update Resource Certificate operation updates the resource/vault credential certificate.|
|/Vaults/delete|The Delete Vault operation deletes the specified Azure resource of type 'vault'|
|/Vaults/extendedInformation/delete|The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault?|
|/Vaults/extendedInformation/read|The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault?|
|/Vaults/extendedInformation/write|The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault?|
|/Vaults/monitoringAlerts/read|Gets the alerts for the Recovery services vault.|
|/Vaults/monitoringAlerts/write|Resolves the alert.|
|/Vaults/monitoringConfigurations/read|Gets the Recovery services vault notification configuration.|
|/Vaults/monitoringConfigurations/write|Configures e-mail notifications to Recovery services vault.|
|/Vaults/providers/Microsoft.Insights/diagnosticSettings/read|Azure Backup Diagnostics|
|/Vaults/providers/Microsoft.Insights/diagnosticSettings/write|Azure Backup Diagnostics|
|/Vaults/providers/Microsoft.Insights/logDefinitions/read|Azure Backup Logs|
|/Vaults/providers/Microsoft.Insights/metricDefinitions/read|Azure Backup Metrics|
|/Vaults/read|The Get Vault operation gets an object representing the Azure resource of type 'vault'|
|/Vaults/registeredIdentities/delete|The UnRegister Container operation can be used to unregister a container.|
|/Vaults/registeredIdentities/operationResults/read|The Get Operation Results operation can be used get the operation status and result for the asynchronously submitted operation|
|/Vaults/registeredIdentities/read|The Get Containers operation can be used get the containers registered for a resource.|
|/Vaults/registeredIdentities/write|The Register Service Container operation can be used to register a container with Recovery Service.|
|/vaults/replicationAlertSettings/read|Read Any Alerts Settings|
|/vaults/replicationAlertSettings/write|Create or Update Any Alerts Settings|
|/vaults/replicationEvents/read|Read Any Events|
|/vaults/replicationFabrics/checkConsistency/action|Checks Consistency of the Fabric|
|/vaults/replicationFabrics/delete|Delete Any Fabrics|
|/vaults/replicationFabrics/deployProcessServerImage/action|Deploy Process Server Image|
|/vaults/replicationFabrics/read|Read Any Fabrics|
|/vaults/replicationFabrics/reassociateGateway/action|Reassociate Gateway|
|/vaults/replicationFabrics/remove/action|Remove Fabric|
|/vaults/replicationFabrics/renewcertificate/action|Renew Certificate for Fabric|
|/vaults/replicationFabrics/replicationNetworks/read|Read Any Networks|
|/vaults/replicationFabrics/replicationNetworks/replicationNetworkMappings/delete|Delete Any Network Mappings|
|/vaults/replicationFabrics/replicationNetworks/replicationNetworkMappings/read|Read Any Network Mappings|
|/vaults/replicationFabrics/replicationNetworks/replicationNetworkMappings/write|Create or Update Any Network Mappings|
|/vaults/replicationFabrics/replicationProtectionContainers/ discoverProtectableItem/action|Discover Protectable Item|
|/vaults/replicationFabrics/replicationProtectionContainers/read|Read Any Protection Containers|
|/vaults/replicationFabrics/replicationProtectionContainers/remove/action|Remove Protection Container|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectableItems/read|Read Any Protectable Items|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/applyRecoveryPoint/action|Apply Recovery Point|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/delete|Delete Any Protected Items|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/failoverCommit/action|Failover Commit|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/plannedFailover/action|Planned Failover|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/read|Read Any Protected Items|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/recoveryPoints/read|Read Any Replication Recovery Points|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/remove/action|Remove Protected Item|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/repairReplication/action|Repair replication|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/reProtect/action|ReProtect Protected Item|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/testFailover/action|Test Failover|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/testFailoverCleanup/action|Test Failover Cleanup|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/unplannedFailover/action|Failover|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/updateMobilityService/action|Update Mobility Service|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectedItems/write|Create or Update Any Protected Items|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectionContainerMappings/delete|Delete Any Protection Container Mappings|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectionContainerMappings/read|Read Any Protection Container Mappings|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectionContainerMappings/remove/action|Remove Protection Container Mapping|
|/vaults/replicationFabrics/replicationProtectionContainers/ replicationProtectionContainerMappings/write|Create or Update Any Protection Container Mappings|
|/vaults/replicationFabrics/replicationProtectionContainers/switchprotection/action|Switch Protection Container|
|/vaults/replicationFabrics/replicationProtectionContainers/write|Create or Update Any Protection Containers|
|/vaults/replicationFabrics/replicationRecoveryServicesProviders/delete|Delete Any Recovery Services Providers|
|/vaults/replicationFabrics/replicationRecoveryServicesProviders/read|Read Any Recovery Services Providers|
|/vaults/replicationFabrics/replicationRecoveryServicesProviders/ refreshProvider/action|Refresh Provider|
|/vaults/replicationFabrics/replicationRecoveryServicesProviders/remove/action|Remove Recovery Services Provider|
|/vaults/replicationFabrics/replicationRecoveryServicesProviders/write|Create or Update Any Recovery Services Providers|
|/vaults/replicationFabrics/replicationStorageClassifications/read|Read Any Storage Classifications|
|/vaults/replicationFabrics/replicationStorageClassifications/ replicationStorageClassificationMappings/delete|Delete Any Storage Classification Mappings|
|/vaults/replicationFabrics/replicationStorageClassifications/ replicationStorageClassificationMappings/read|Read Any Storage Classification Mappings|
|/vaults/replicationFabrics/replicationStorageClassifications/ replicationStorageClassificationMappings/write|Create or Update Any Storage Classification Mappings|
|/vaults/replicationFabrics/replicationvCenters/delete|Delete Any Jobs|
|/vaults/replicationFabrics/replicationvCenters/read|Read Any Jobs|
|/vaults/replicationFabrics/replicationvCenters/write|Create or Update Any Jobs|
|/vaults/replicationFabrics/write|Create or Update Any Fabrics|
|/vaults/replicationJobs/cancel/action|Cancel Job|
|/vaults/replicationJobs/read|Read Any Jobs|
|/vaults/replicationJobs/restart/action|Restart job|
|/vaults/replicationJobs/resume/action|Resume Job|
|/vaults/replicationPolicies/delete|Delete Any Policies|
|/vaults/replicationPolicies/read|Read Any Policies|
|/vaults/replicationPolicies/write|Create or Update Any Policies|
|/vaults/replicationRecoveryPlans/delete|Delete Any Recovery Plans|
|/vaults/replicationRecoveryPlans/failoverCommit/action|Failover Commit Recovery Plan|
|/vaults/replicationRecoveryPlans/plannedFailover/action|Planned Failover Recovery Plan|
|/vaults/replicationRecoveryPlans/read|Read Any Recovery Plans|
|/vaults/replicationRecoveryPlans/reProtect/action|ReProtect Recovery Plan|
|/vaults/replicationRecoveryPlans/testFailover/action|Test Failover Recovery Plan|
|/vaults/replicationRecoveryPlans/testFailoverCleanup/action|Test Failover Cleanup Recovery Plan|
|/vaults/replicationRecoveryPlans/unplannedFailover/action|Failover Recovery Plan|
|/vaults/replicationRecoveryPlans/write|Create or Update Any Recovery Plans|
|/Vaults/tokenInfo/read|Returns token information for Recovery Services Vault.|
|/vaults/usages/read|Read Any Vault Usages|
|/Vaults/usages/read|Returns usage details for a Recovery Services Vault.|
|/Vaults/vaultTokens/read|The Vault Token operation can be used to get Vault Token for vault level backend operations.|
|/Vaults/write|Create Vault operation creates an Azure resource of type 'vault'|

## <a name="microsoftrelay"></a>Microsoft.Relay

| Operation | Description |
|---|---|
|/checkNameAvailability/action|Checks availability of namespace under given subscription.|
|/checkNamespaceAvailability/action|Checks availability of namespace under given subscription. This API is deprecated please use CheckNameAvailabiltiy instead.|
|/namespaces/authorizationRules/action|Updates Namespace Authorization Rule. This API is depricated. Please use a PUT call to update the Namespace Authorization Rule instead.. This operation is not supported on API version 2017-04-01.|
|/namespaces/authorizationRules/delete|Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted. |
|/namespaces/authorizationRules/listkeys/action|Get the Connection String to the Namespace|
|/namespaces/authorizationRules/read|Get the list of Namespaces Authorization Rules description.|
|/namespaces/authorizationRules/regenerateKeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/authorizationRules/write|Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated.|
|/namespaces/Delete|Delete Namespace Resource|
|/namespaces/disasterRecoveryConfigs/authorizationRules/listkeys/action|Gets the authorization rules keys for the Disaster Recovery primary namespace|
|/namespaces/disasterRecoveryConfigs/authorizationRules/read|Get Disaster Recovery Primary Namespace's Authorization Rules|
|/namespaces/disasterRecoveryConfigs/breakPairing/action|Disables Disaster Recovery and stops replicating changes from primary to secondary namespaces.|
|/namespaces/disasterrecoveryconfigs/checkNameAvailability/action|Checks availability of namespace alias under given subscription.|
|/namespaces/disasterRecoveryConfigs/delete|Deletes the Disaster Recovery configuration associated with the namespace. This operation can only be invoked via the primary namespace.|
|/namespaces/disasterRecoveryConfigs/failover/action|Invokes a GEO DR failover and reconfigures the namespace alias to point to the secondary namespace.|
|/namespaces/disasterRecoveryConfigs/read|Gets the Disaster Recovery configuration associated with the namespace.|
|/namespaces/disasterRecoveryConfigs/write|Creates or Updates the Disaster Recovery configuration associated with the namespace.|
|/namespaces/HybridConnections/authorizationRules/action|Operation to update HybridConnection. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule.|
|/namespaces/HybridConnections/authorizationRules/delete|Operation to delete HybridConnection Authorization Rules|
|/namespaces/HybridConnections/authorizationRules/listkeys/action|Get the Connection String to HybridConnection|
|/namespaces/HybridConnections/authorizationRules/read| Get the list of HybridConnection Authorization Rules|
|/namespaces/HybridConnections/authorizationRules/regeneratekeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/HybridConnections/authorizationRules/write|Create HybridConnection Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated.|
|/namespaces/HybridConnections/Delete|Operation to delete HybridConnection Resource|
|/namespaces/HybridConnections/read|Get list of HybridConnection Resource Descriptions|
|/namespaces/HybridConnections/write|Create or Update HybridConnection properties.|
|/namespaces/messagingPlan/read|Gets the Messaging Plan for a namespace. This API is deprecated. Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions.. This operation is not supported on API version 2017-04-01.|
|/namespaces/messagingPlan/write|Updates the Messaging Plan for a namespace. This API is deprecated. Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions.. This operation is not supported on API version 2017-04-01.|
|/namespaces/operationresults/read|Get the status of Namespace operation|
|/namespaces/providers/Microsoft.Insights/metricDefinitions/read|Get list of Namespace metrics Resource Descriptions|
|/namespaces/read|Get the list of Namespace Resource Description|
|/namespaces/WcfRelays/authorizationRules/action|Operation to update WcfRelay. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule.|
|/namespaces/WcfRelays/authorizationRules/delete|Operation to delete WcfRelay Authorization Rules|
|/namespaces/WcfRelays/authorizationRules/listkeys/action|Get the Connection String to WcfRelay|
|/namespaces/WcfRelays/authorizationRules/read| Get the list of WcfRelay Authorization Rules|
|/namespaces/WcfRelays/authorizationRules/regeneratekeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/WcfRelays/authorizationRules/write|Create WcfRelay Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated.|
|/namespaces/WcfRelays/Delete|Operation to delete WcfRelay Resource|
|/namespaces/WcfRelays/read|Get list of WcfRelay Resource Descriptions|
|/namespaces/WcfRelays/write|Create or Update WcfRelay properties.|
|/namespaces/write|Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated.|
|/operations/read|Get Operations|
|/register/action|Registers the subscription for the Relay resource provider and enables the creation of Relay resources|
|/unregister/action|Registers the subscription for the Relay resource provider and enables the creation of Relay resources|

## <a name="microsoftresourcehealth"></a>Microsoft.ResourceHealth

| Operation | Description |
|---|---|
|/AvailabilityStatuses/current/read|Gets the availability status for the specified resource|
|/AvailabilityStatuses/read|Gets the availability statuses for all resources in the specified scope|
|/healthevent/action|Denotes the change in health state for the specified resource|
|/healthevent/Activated/action|Denotes the change in health state for the specified resource|
|/healthevent/InProgress/action|Denotes the change in health state for the specified resource|
|/healthevent/Pending/action|Denotes the change in health state for the specified resource|
|/healthevent/Resolved/action|Denotes the change in health state for the specified resource|
|/healthevent/Updated/action|Denotes the change in health state for the specified resource|
|/register/action|Registers the subscription for the Microsoft ResourceHealth|

## <a name="microsoftresources"></a>Microsoft.Resources

| Operation | Description |
|---|---|
|/checkResourceName/action|Check the resource name for validity.|
|/deployments/cancel/action|Cancels a deployment.|
|/deployments/delete|Deletes a deployment.|
|/deployments/operations/read|Gets or lists deployment operations.|
|/deployments/read|Gets or lists deployments.|
|/deployments/validate/action|Validates an deployment.|
|/deployments/write|Creates or updates an deployment.|
|/links/delete|Deletes a resource link.|
|/links/read|Gets or lists resource links.|
|/links/write|Creates or updates a resource link.|
|/marketplace/purchase/action|Purchases a resource from the marketplace.|
|/providers/read|Get the list of providers.|
|/resources/read|Get the list of resources based upon filters.|
|/subscriptions/locations/read|Gets the list of locations supported.|
|/subscriptions/operationresults/read|Get the subscription operation results.|
|/subscriptions/providers/read|Gets or lists resource providers.|
|/subscriptions/read|Gets the list of subscriptions.|
|/subscriptions/resourceGroups/delete|Deletes a resource group and all its resources.|
|/subscriptions/resourcegroups/deployments/operations/read|Gets or lists deployment operations.|
|/subscriptions/resourcegroups/deployments/operationstatuses/read|Gets or lists deployment operation statuses.|
|/subscriptions/resourcegroups/deployments/read|Gets or lists deployments.|
|/subscriptions/resourcegroups/deployments/write|Creates or updates an deployment.|
|/subscriptions/resourceGroups/moveResources/action|Moves resources from one resource group to another.|
|/subscriptions/resourceGroups/read|Gets or lists resource groups.|
|/subscriptions/resourcegroups/resources/read|Gets the resources for the resource group.|
|/subscriptions/resourceGroups/validateMoveResources/action|Validate move of resources from one resource group to another.|
|/subscriptions/resourceGroups/write|Creates or updates a resource group.|
|/subscriptions/resources/read|Gets resources of a subscription.|
|/subscriptions/tagNames/delete|Deletes a subscription tag.|
|/subscriptions/tagNames/read|Gets or lists subscription tags.|
|/subscriptions/tagNames/tagValues/delete|Deletes a subscription tag value.|
|/subscriptions/tagNames/tagValues/read|Gets or lists subscription tag values.|
|/subscriptions/tagNames/tagValues/write|Adds a subscription tag value.|
|/subscriptions/tagNames/write|Adds a subscription tag.|
|/tenants/read|Gets the list of tenants.|

## <a name="microsoftscheduler"></a>Microsoft.Scheduler

| Operation | Description |
|---|---|
|/jobcollections/delete|Deletes job collection.|
|/jobcollections/disable/action|Disables job collection.|
|/jobcollections/enable/action|Enables job collection.|
|/jobcollections/jobs/delete|Deletes job.|
|/jobcollections/jobs/generateLogicAppDefinition/action|Generates Logic App definition based on a Scheduler Job.|
|/jobcollections/jobs/jobhistories/read|Gets job history.|
|/jobcollections/jobs/read|Gets job.|
|/jobcollections/jobs/run/action|Runs job.|
|/jobcollections/jobs/write|Creates or updates job.|
|/jobcollections/read|Get Job Collection|
|/jobcollections/write|Creates or updates job collection.|

## <a name="microsoftsearch"></a>Microsoft.Search

| Operation | Description |
|---|---|
|/checkNameAvailability/action|Checks availability of the service name.|
|/register/action|Registers the subscription for the search resource provider and enables the creation of search services.|
|/searchServices/createQueryKey/action|Creates the query key.|
|/searchServices/delete|Deletes the search service.|
|/searchServices/diagnosticSettings/read|Gets the diganostic setting read for the resource|
|/searchServices/diagnosticSettings/write|Creates or updates the diganostic setting for the resource|
|/searchServices/listAdminKeys/action|Reads the admin keys.|
|/searchServices/logDefinitions/read|Gets the available logs for the search service|
|/searchServices/metricDefinitions/read|Gets the available metrics for the search service|
|/searchServices/queryKey/delete|Deletes the query key.|
|/searchServices/queryKey/read|Reads the query keys.|
|/searchServices/read|Reads the search service.|
|/searchServices/regenerateAdminKey/action|Regenerates the admin key.|
|/searchServices/start/action|Starts the search service.|
|/searchServices/stop/action|Stops the search service.|
|/searchServices/write|Creates or updates the search service.|

## <a name="microsoftsecurity"></a>Microsoft.Security

| Operation | Description |
|---|---|
|/alerts/read|Gets all available security alerts|
|/applicationWhitelistings/read|Gets the application whitelistings|
|/applicationWhitelistings/write|Creates a new application whitelisting or updates an existing one|
|/complianceResults/read|Gets the compliance results for the resource|
|/locations/alerts/activate/action|Activate a security alert|
|/locations/alerts/dismiss/action|Dismiss a security alert|
|/locations/alerts/read|Gets all available security alerts|
|/locations/jitNetworkAccessPolicies/initiate/action|Initiates a just-in-time network access policy|
|/locations/jitNetworkAccessPolicies/read|Gets the just-in-time network access policies|
|/locations/jitNetworkAccessPolicies/write|Creates a new just-in-time network access policy or updates an existing one|
|/locations/read|Gets the security data location|
|/locations/tasks/activate/action|Activate a security recommendation|
|/locations/tasks/dismiss/action|Dismiss a security recommendation|
|/locations/tasks/read|Gets all available security recommendations|
|/locations/tasks/resolve/action|Resolve a security recommendation|
|/locations/tasks/start/action|Start a security recommendation|
|/policies/read|Gets the security policy|
|/policies/write|Updates the security policy|
|/pricings/delete|Deletes the pricing settings for the scope|
|/pricings/read|Gets the pricing settings for the scope|
|/pricings/write|Updates the pricing settings for the scope|
|/register/action|Registers the subscription for Azure Security Center|
|/securityContacts/delete|Deletes the security contact|
|/securityContacts/read|Gets the security contact|
|/securityContacts/write|Updates the security contact|
|/securitySolutions/delete|Deletes a security solution|
|/securitySolutions/read|Gets the security solutions|
|/securitySolutions/write|Creates a new security solution or updates an existing one|
|/securitySolutionsReferenceData/read|Gets the security solutions reference data|
|/securityStatuses/read|Gets the security health statuses for Azure resources|
|/securityStatusesSummaries/read|Gets the security statuses summaries for the scope|
|/tasks/read|Gets all available security recommendations|
|/webApplicationFirewalls/delete|Deletes a web application firewall|
|/webApplicationFirewalls/read|Gets the web application firewalls|
|/webApplicationFirewalls/write|Creates a new web application firewall or updates an existing one|
|/workspaceSettings/connect/action|Change workspace settings reconnection settings|
|/workspaceSettings/delete|Deletes the workspace settings|
|/workspaceSettings/read|Gets the workspace settings|
|/workspaceSettings/write|Updates the workspace settings|

## <a name="microsoftservicebus"></a>Microsoft.ServiceBus

| Operation | Description |
|---|---|
|/checkNameAvailability/action|Checks availability of namespace under given subscription.|
|/checkNamespaceAvailability/action|Checks availability of namespace under given subscription. This API is deprecated please use CheckNameAvailabiltiy instead.|
|/namespaces/authorizationRules/action|Updates Namespace Authorization Rule. This API is depricated. Please use a PUT call to update the Namespace Authorization Rule instead.. This operation is not supported on API version 2017-04-01.|
|/namespaces/authorizationRules/delete|Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted. |
|/namespaces/authorizationRules/listkeys/action|Get the Connection String to the Namespace|
|/namespaces/authorizationRules/read|Get the list of Namespaces Authorization Rules description.|
|/namespaces/authorizationRules/regenerateKeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/authorizationRules/write|Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated.|
|/namespaces/Delete|Delete Namespace Resource|
|/namespaces/disasterRecoveryConfigs/authorizationRules/listkeys/action|Gets the authorization rules keys for the Disaster Recovery primary namespace|
|/namespaces/disasterRecoveryConfigs/authorizationRules/read|Get Disaster Recovery Primary Namespace's Authorization Rules|
|/namespaces/disasterRecoveryConfigs/breakPairing/action|Disables Disaster Recovery and stops replicating changes from primary to secondary namespaces.|
|/namespaces/disasterrecoveryconfigs/checkNameAvailability/action|Checks availability of namespace alias under given subscription.|
|/namespaces/disasterRecoveryConfigs/delete|Deletes the Disaster Recovery configuration associated with the namespace. This operation can only be invoked via the primary namespace.|
|/namespaces/disasterRecoveryConfigs/failover/action|Invokes a GEO DR failover and reconfigures the namespace alias to point to the secondary namespace.|
|/namespaces/disasterRecoveryConfigs/read|Gets the Disaster Recovery configuration associated with the namespace.|
|/namespaces/disasterRecoveryConfigs/write|Creates or Updates the Disaster Recovery configuration associated with the namespace.|
|/namespaces/eventGridFilters/delete|Deletes the Event Grid filter associated with the namespace.|
|/namespaces/eventGridFilters/read|Gets the Event Grid filter associated with the namespace.|
|/namespaces/eventGridFilters/write|Creates or Updates the Event Grid filter associated with the namespace.|
|/namespaces/eventhubs/read|Get list of EventHub Resource Descriptions|
|/namespaces/messagingPlan/read|Gets the Messaging Plan for a namespace. This API is deprecated. Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions.. This operation is not supported on API version 2017-04-01.|
|/namespaces/messagingPlan/write|Updates the Messaging Plan for a namespace. This API is deprecated. Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions.. This operation is not supported on API version 2017-04-01.|
|/namespaces/migrate/action|Migrate namespace operation|
|/namespaces/operationresults/read|Get the status of Namespace operation|
|/namespaces/providers/Microsoft.Insights/diagnosticSettings/read|Get list of Namespace diagnostic settings Resource Descriptions|
|/namespaces/providers/Microsoft.Insights/diagnosticSettings/write|Get list of Namespace diagnostic settings Resource Descriptions|
|/namespaces/providers/Microsoft.Insights/logDefinitions/read|Get list of Namespace logs Resource Descriptions|
|/namespaces/providers/Microsoft.Insights/metricDefinitions/read|Get list of Namespace metrics Resource Descriptions|
|/namespaces/queues/authorizationRules/action|Operation to update Queue. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule.|
|/namespaces/queues/authorizationRules/delete|Operation to delete Queue Authorization Rules|
|/namespaces/queues/authorizationRules/listkeys/action|Get the Connection String to Queue|
|/namespaces/queues/authorizationRules/read| Get the list of Queue Authorization Rules|
|/namespaces/queues/authorizationRules/regenerateKeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/queues/authorizationRules/write|Create Queue Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated.|
|/namespaces/queues/Delete|Operation to delete Queue Resource|
|/namespaces/queues/read|Get list of Queue Resource Descriptions|
|/namespaces/queues/write|Create or Update Queue properties.|
|/namespaces/read|Get the list of Namespace Resource Description|
|/namespaces/topics/authorizationRules/action|Operation to update Topic. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule.|
|/namespaces/topics/authorizationRules/delete|Operation to delete Topic Authorization Rules|
|/namespaces/topics/authorizationRules/listkeys/action|Get the Connection String to Topic|
|/namespaces/topics/authorizationRules/read| Get the list of Topic Authorization Rules|
|/namespaces/topics/authorizationRules/regenerateKeys/action|Regenerate the Primary or Secondary key to the Resource|
|/namespaces/topics/authorizationRules/write|Create Topic Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated.|
|/namespaces/topics/Delete|Operation to delete Topic Resource|
|/namespaces/topics/read|Get list of Topic Resource Descriptions|
|/namespaces/topics/subscriptions/Delete|Operation to delete TopicSubscription Resource|
|/namespaces/topics/subscriptions/read|Get list of TopicSubscription Resource Descriptions|
|/namespaces/topics/subscriptions/rules/Delete|Operation to delete Rule Resource|
|/namespaces/topics/subscriptions/rules/read|Get list of Rule Resource Descriptions|
|/namespaces/topics/subscriptions/rules/write|Create or Update Rule properties.|
|/namespaces/topics/subscriptions/write|Create or Update TopicSubscription properties.|
|/namespaces/topics/write|Create or Update Topic properties.|
|/namespaces/write|Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated.|
|/operations/read|Get Operations|
|/register/action|Registers the subscription for the ServiceBus resource provider and enables the creation of ServiceBus resources|
|/sku/read|Get list of Sku Resource Descriptions|
|/sku/regions/read|Get list of SkuRegions Resource Descriptions|
|/unregister/action|Registers the subscription for the ServiceBus resource provider and enables the creation of ServiceBus resources|

## <a name="microsoftservicefabric"></a>Microsoft.ServiceFabric

| Operation | Description |
|---|---|
|/clusters/applications/delete|Delete any Application|
|/clusters/applications/read|Read any Application|
|/clusters/applications/services/delete|Delete any Service|
|/clusters/applications/services/partitions/read|Read any Partition|
|/clusters/applications/services/partitions/replicas/read|Read any Replica|
|/clusters/applications/services/read|Read any Service|
|/clusters/applications/services/statuses/read|Read any Service Status|
|/clusters/applications/services/write|Create or Update any Service|
|/clusters/applications/write|Create or Update any Application|
|/clusters/applicationTypes/delete|Delete any Application Type|
|/clusters/applicationTypes/read|Read any Application Type|
|/clusters/applicationTypes/versions/delete|Delete any Application Type Version|
|/clusters/applicationTypes/versions/read|Read any Application Type Version|
|/clusters/applicationTypes/versions/write|Create or Update any Application Type Version|
|/clusters/applicationTypes/write|Create or Update any Application Type|
|/clusters/delete|Delete any Cluster|
|/clusters/nodes/read|Read any Node|
|/clusters/read|Read any Cluster|
|/clusters/statuses/read|Read any Cluster Status|
|/clusters/write|Create or Update any Cluster|
|/locations/clusterVersions/read|Read any Cluster Version|
|/locations/environments/clusterVersions/read|Read any Cluster Version for a specific environment|
|/locations/operationresults/read|Read any Operation Results|
|/locations/operations/read|Read any Operations by location|
|/operations/read|Read any Available Operations|
|/register/action|Register any Action|

## <a name="microsoftsolutions"></a>Microsoft.Solutions

| Operation | Description |
|---|---|
|/applicationDefinitions/delete|Removes an application definition.|
|/applicationDefinitions/read|Retrieves a list of application definitions.|
|/applicationDefinitions/write|Add or modify an application definition.|
|/applications/delete|Removes an application.|
|/applications/read|Retrieves a list of applications.|
|/applications/write|Creates an application.|
|/locations/operationStatuses/read|Reads the operation status for the resource.|
|/register/action|Register to Solutions.|

## <a name="microsoftsql"></a>Microsoft.Sql

| Operation | Description |
|---|---|
|/checkNameAvailability/action|Verify whether given server name is available for provisioning worldwide for a given subscription.|
|/locations/auditingSettingsAzureAsyncOperation/read|Retrieve result of the extended server blob auditing policy Set operation|
|/locations/auditingSettingsOperationResults/read|Retrieve result of the server blob auditing policy Set operation|
|/locations/capabilities/read|Gets the capabilities for this subscription in a given location|
|/locations/databaseAzureAsyncOperation/read|Gets the status of a database operation.|
|/locations/databaseOperationResults/read|Gets the status of a database operation.|
|/locations/deletedServerAsyncOperation/read|Gets in-progress operations on deleted server|
|/locations/deletedServerOperationResults/read|Gets in-progress operations on deleted server|
|/locations/deletedServers/read|Return the list of deleted servers or gets the properties for the specified deleted server.|
|/locations/deletedServers/recover/action|Recover a deleted server|
|/locations/deleteVirtualNetworkOrSubnets/action|Deletes Virtual network rules associated to a virtual network or subnet|
|/locations/elasticPoolAzureAsyncOperation/read|Gets the azure async operation for an elastic pool async operation|
|/locations/elasticPoolOperationResults/read|Gets the result of an elastic pool operation.|
|/locations/extendedAuditingSettingsAzureAsyncOperation/read|Retrieve result of the extended server blob auditing policy Set operation|
|/locations/extendedAuditingSettingsOperationResults/read|Retrieve result of the extended server blob auditing policy Set operation|
|/locations/managedDatabaseRestoreAzureAsyncOperation/completeRestore/action|Completes managed database restore operation|
|/locations/managedTransparentDataEncryptionAzureAsyncOperation/read|Gets in-progress operations on managed database transparent data encryption|
|/locations/managedTransparentDataEncryptionOperationResults/read|Gets in-progress operations on managed database transparent data encryption|
|/locations/read|Gets the available locations for a given subscription|
|/locations/syncAgentOperationResults/read|Retrieve result of the sync agent resource operation|
|/locations/syncDatabaseIds/read|Retrieve the sync database ids for a particular region and subscription|
|/locations/syncGroupOperationResults/read|Retrieve result of the sync group resource operation|
|/locations/syncMemberOperationResults/read|Retrieve result of the sync member resource operation|
|/locations/usages/read|Gets a collection of usage metrics for this subscription in a location|
|/locations/virtualNetworkRulesAzureAsyncOperation/read|Returns the details of the specified virtual network rules azure async operation |
|/locations/virtualNetworkRulesOperationResults/read|Returns the details of the specified virtual network rules operation |
|/managedInstances/administrators/delete|Deletes an existing administrator of managed instance.|
|/managedInstances/administrators/read|Gets a list of managed instance administrators.|
|/managedInstances/administrators/write|Creates or updates managed instance administrator with the specified parameters.|
|/managedInstances/databases/delete|Deletes an existing managed database|
|/managedInstances/databases/read|Gets existing managed database|
|/managedInstances/databases/securityAlertPolicies/read|Retrieve details of the database threat detection policy configured on a given managed database|
|/managedInstances/databases/securityAlertPolicies/write|Change the database threat detection policy for a given managed database|
|/managedInstances/databases/securityEvents/read|Retrieves the managed database security events|
|/managedInstances/databases/transparentDataEncryption/read|Retrieve details of the database Transparent Data Encryption on a given managed database|
|/managedInstances/databases/transparentDataEncryption/write|Change the database Transparent Data Encryption for a given managed database|
|/managedInstances/databases/write|Creates a new database or updates an existing database.|
|/managedInstances/delete|Deletes an existing  managed instance.|
|/managedInstances/metricDefinitions/read|Get managed instance metric definitions|
|/managedInstances/metrics/read|Get managed instance metrics|
|/managedInstances/read|Return the list of managed instances or gets the properties for the specified managed instance.|
|/managedInstances/securityAlertPolicies/read|Retrieve details of the managed server threat detection policy configured on a given managed server|
|/managedInstances/securityAlertPolicies/write|Change the managed server threat detection policy for a given managed server|
|/managedInstances/write|Creates a managed instance with the specified parameters or update the properties or tags for the specified managed instance.|
|/operations/read|Gets available REST operations|
|/register/action|Registers the subscription for the Microsoft SQL Database resource provider and enables the creation of Microsoft SQL Databases.|
|/servers/administratorOperationResults/read|Gets in-progress operations on server administrators|
|/servers/administrators/delete|Delete server administrator|
|/servers/administrators/read|Retrieve server administrator details|
|/servers/administrators/write|Create or update server administrator|
|/servers/advisors/read|Returns list of advisors available for the server|
|/servers/advisors/recommendedActions/read|Returns list of recommended actions of specified advisor for the server|
|/servers/advisors/recommendedActions/write|Apply the recommended action on the server|
|/servers/advisors/write|Updates auto-execute status of an advisor on server level.|
|/servers/auditingPolicies/read|Retrieve details of the default server table auditing policy configured on a given server|
|/servers/auditingPolicies/write|Change the default server table auditing for a given server|
|/servers/auditingSettings/operationResults/read|Retrieve result of the server blob auditing policy Set operation|
|/servers/auditingSettings/read|Retrieve details of the server blob auditing policy configured on a given server|
|/servers/auditingSettings/write|Change the server blob auditing for a given server|
|/servers/automaticTuning/read|Returns automatic tuning settings for the server|
|/servers/automaticTuning/write|Updates automatic tuning settings for the server and returns updated settings|
|/servers/backupLongTermRetentionVaults/delete|Deletes an existing backup archival vault.|
|/servers/backupLongTermRetentionVaults/read|This operation is used to get a backup long term retention vault. It returns information about the vault registered to this server|
|/servers/backupLongTermRetentionVaults/write|This operation is used to register a backup long term retention vault to a server|
|/servers/communicationLinks/delete|Deletes an existing server communication link.|
|/servers/communicationLinks/read|Return the list of communication links of a specified server.|
|/servers/communicationLinks/write|Create or update a server communication link.|
|/servers/connectionPolicies/read|Return the list of server connection policies of a specified server.|
|/servers/connectionPolicies/write|Create or update a server connection policy.|
|/servers/databases/advisors/read|Returns list of advisors available for the database|
|/servers/databases/advisors/recommendedActions/read|Returns list of recommended actions of specified advisor for the database|
|/servers/databases/advisors/recommendedActions/write|Apply the recommended action on the database|
|/servers/databases/advisors/write|Update auto-execute status of an advisor on database level.|
|/servers/databases/auditingPolicies/read|Retrieve details of the table auditing policy configured on a given database|
|/servers/databases/auditingPolicies/write|Change the table auditing policy for a given database|
|/servers/databases/auditingSettings/read|Retrieve details of the blob auditing policy configured on a given database|
|/servers/databases/auditingSettings/write|Change the blob auditing policy for a given database|
|/servers/databases/auditRecords/read|Retrieve the database blob audit records|
|/servers/databases/automaticTuning/read|Returns automatic tuning settings for a database|
|/servers/databases/automaticTuning/write|Updates automatic tuning settings for a database and returns updated settings|
|/servers/databases/azureAsyncOperation/read|Gets the status of a database operation.|
|/servers/databases/backupLongTermRetentionPolicies/read|Return the list of backup archival policies of a specified database.|
|/servers/databases/backupLongTermRetentionPolicies/write|Create or update a database backup archival policy.|
|/servers/databases/connectionPolicies/read|Retrieve details of the connection policy configured on a given database|
|/servers/databases/connectionPolicies/write|Change connection policy for a given database|
|/servers/databases/dataMaskingPolicies/read|Return the list of database data masking policies.|
|/servers/databases/dataMaskingPolicies/rules/delete|Delete data masking policy rule for a given database|
|/servers/databases/dataMaskingPolicies/rules/read|Retrieve details of the data masking policy rule configured on a given database|
|/servers/databases/dataMaskingPolicies/rules/write|Change data masking policy rule for a given database|
|/servers/databases/dataMaskingPolicies/write|Change data masking policy for a given database|
|/servers/databases/dataWarehouseQueries/dataWarehouseQuerySteps/read|Returns the distributed query step information of data warehouse query for selected step ID|
|/servers/databases/dataWarehouseQueries/read|Returns the data warehouse distribution query information for selected query ID|
|/servers/databases/dataWarehouseUserActivities/read|Retrieves the user activities of a SQL Data Warehouse instance which includes running and suspended queries|
|/servers/databases/delete|Deletes an existing database.|
|/servers/databases/export/action|Export Azure SQL Database|
|/servers/databases/extendedAuditingSettings/read|Retrieve details of the extended blob auditing policy configured on a given database|
|/servers/databases/extendedAuditingSettings/write|Change the extended blob auditing policy for a given database|
|/servers/databases/extensions/read|Gets a collection of extensions for the database.|
|/servers/databases/extensions/write|Change the extension for a given database|
|/servers/databases/geoBackupPolicies/read|Retrieve geo backup policies for a given database|
|/servers/databases/geoBackupPolicies/write|Create or update a database geobackup policy|
|/servers/databases/importExportOperationResults/read|Gets in-progress import/export operations|
|/servers/databases/metricDefinitions/read|Return types of metrics that are available for databases|
|/servers/databases/metrics/read|Return metrics for databases|
|/servers/databases/move/action|Rename Azure SQL Database|
|/servers/databases/operationResults/read|Gets the status of a database operation.|
|/servers/databases/operations/cancel/action|Cancels Azure SQL Database pending asynchronous operation that is not finished yet.|
|/servers/databases/operations/read|Return the list of operations performed on the database|
|/servers/databases/pause/action|Pause Azure SQL Datawarehouse Database|
|/servers/databases/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/servers/databases/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/servers/databases/providers/Microsoft.Insights/logDefinitions/read|Gets the available logs for databases|
|/servers/databases/providers/Microsoft.Insights/metricDefinitions/read|Return types of metrics that are available for databases|
|/servers/databases/queryStore/queryTexts/read|Returns the collection of query texts that correspond to the specified parameters.|
|/servers/databases/queryStore/read|Returns current values of Query Store settings for the database.|
|/servers/databases/queryStore/write|Updates Query Store setting for the database|
|/servers/databases/read|Return the list of databases or gets the properties for the specified database.|
|/servers/databases/replicationLinks/delete|Terminate the replication relationship forcefully and with potential data loss|
|/servers/databases/replicationLinks/failover/action|Failover after synchronizing all changes from the primary, making this database into the replication relationship\u0027s primary and making the remote primary into a secondary|
|/servers/databases/replicationLinks/forceFailoverAllowDataLoss/action|Failover immediately with potential data loss, making this database into the replication relationship\u0027s primary and making the remote primary into a secondary|
|/servers/databases/replicationLinks/read|Return details about replication links established for a particular database|
|/servers/databases/replicationLinks/unlink/action|Terminate the replication relationship forcefully or after synchronizing with the partner|
|/servers/databases/replicationLinks/updateReplicationMode/action|Update replication mode for link to synchronous or asynchronous mode|
|/servers/databases/restorePoints/action|Creates a new restore point|
|/servers/databases/restorePoints/read|Returns restore points for the database.|
|/servers/databases/resume/action|Resume Azure SQL Datawarehouse Database|
|/servers/databases/schemas/read|Retrieve list of schemas of a database|
|/servers/databases/schemas/tables/columns/read|Retrieve list of columns of a table|
|/servers/databases/schemas/tables/columns/sensitivityLabels/delete|Delete the sensitivity label of a given column|
|/servers/databases/schemas/tables/columns/sensitivityLabels/read|Get the sensitivity label of a given column|
|/servers/databases/schemas/tables/columns/sensitivityLabels/write|Create or update the sensitivity label of a given column|
|/servers/databases/schemas/tables/read|Retrieve list of tables of a database|
|/servers/databases/schemas/tables/recommendedIndexes/read|Retrieve list of index recommendations on a database|
|/servers/databases/schemas/tables/recommendedIndexes/write|Apply index recommendation|
|/servers/databases/securityAlertPolicies/read|Retrieve details of the threat detection policy configured on a given database|
|/servers/databases/securityAlertPolicies/write|Change the threat detection policy for a given database|
|/servers/databases/securityMetrics/read|Gets a collection of database security metrics|
|/servers/databases/sensitivityLabels/read|List sensitivity labels of a given database|
|/servers/databases/serviceTierAdvisors/read|Return suggestion about scaling database up or down based on query execution statistics to improve performance or reduce cost|
|/servers/databases/syncGroups/cancelSync/action|Cancel sync group synchronization|
|/servers/databases/syncGroups/delete|Deletes an existing sync group.|
|/servers/databases/syncGroups/hubSchemas/read|Return the list of sync hub database schemas|
|/servers/databases/syncGroups/logs/read|Return the list of sync group logs|
|/servers/databases/syncGroups/read|Return the list of sync groups or gets the properties for the specified sync group.|
|/servers/databases/syncGroups/refreshHubSchema/action|Refresh sync hub database schema|
|/servers/databases/syncGroups/refreshHubSchemaOperationResults/read|Retrieve result of the sync hub schema refresh operation|
|/servers/databases/syncGroups/syncMembers/delete|Deletes an existing sync member.|
|/servers/databases/syncGroups/syncMembers/read|Return the list of sync members or gets the properties for the specified sync member.|
|/servers/databases/syncGroups/syncMembers/refreshSchema/action|Refresh sync member schema|
|/servers/databases/syncGroups/syncMembers/refreshSchemaOperationResults/read|Retrieve result of the sync member schema refresh operation|
|/servers/databases/syncGroups/syncMembers/schemas/read|Return the list of sync member database schemas|
|/servers/databases/syncGroups/syncMembers/write|Creates a sync member with the specified parameters or update the properties for the specified sync member.|
|/servers/databases/syncGroups/triggerSync/action|Trigger sync group synchronization|
|/servers/databases/syncGroups/write|Creates a sync group with the specified parameters or update the properties for the specified sync group.|
|/servers/databases/topQueries/queryText/action|Returns the Transact-SQL text for selected query ID|
|/servers/databases/topQueries/read|Returns aggregated runtime statistics for selected query in selected time period|
|/servers/databases/topQueries/statistics/read|Returns aggregated runtime statistics for selected query in selected time period|
|/servers/databases/transparentDataEncryption/operationResults/read|Gets in-progress operations on transparent data encryption|
|/servers/databases/transparentDataEncryption/read|Retrieve status and details of transparent data encryption security feature for a given database|
|/servers/databases/transparentDataEncryption/write|Change transparent data encryption state|
|/servers/databases/upgradeDataWarehouse/action|Upgrade Azure SQL Datawarehouse Database|
|/servers/databases/usages/read|Gets the Azure SQL Database usages information|
|/servers/databases/vulnerabilityAssessments/delete|Remove the vulnerability assessment for a given database|
|/servers/databases/vulnerabilityAssessments/read|Retrieve details of the vulnerability assessment configured on a given database|
|/servers/databases/vulnerabilityAssessments/rules/baselines/delete|Remove the vulnerability assessment rule baseline for a given database|
|/servers/databases/vulnerabilityAssessments/rules/baselines/read|Get the vulnerability assessment rule baseline for a given database|
|/servers/databases/vulnerabilityAssessments/rules/baselines/write|Change the vulnerability assessment rule baseline for a given database|
|/servers/databases/vulnerabilityAssessments/scans/action|Execute vulnerability assessment database scan.|
|/servers/databases/vulnerabilityAssessments/scans/export/action|Convert an existing scan result to a human readable format. If already exists nothing happens|
|/servers/databases/vulnerabilityAssessments/scans/read|Return the list of database vulnerability assessment scan records or get the scan record for the specified scan ID.|
|/servers/databases/vulnerabilityAssessments/write|Change the vulnerability assessment for a given database|
|/servers/databases/vulnerabilityAssessmentScans/action|Execute vulnerability assessment database scan.|
|/servers/databases/vulnerabilityAssessmentScans/operationResults/read|Retrieve the result of the database vulnerability assessment scan Execute operation|
|/servers/databases/vulnerabilityAssessmentSettings/read|Retrieve details of the vulnerability assessment configured on a given database|
|/servers/databases/vulnerabilityAssessmentSettings/write|Change the vulnerability assessment for a given database|
|/servers/databases/write|Creates a database with the specified parameters or update the properties or tags for the specified database.|
|/servers/delete|Deletes an existing server.|
|/servers/disasterRecoveryConfiguration/delete|Deletes an existing disaster recovery configurations for a given server|
|/servers/disasterRecoveryConfiguration/failover/action|Failover a DisasterRecoveryConfiguration|
|/servers/disasterRecoveryConfiguration/forceFailoverAllowDataLoss/action|Force Failover a DisasterRecoveryConfiguration|
|/servers/disasterRecoveryConfiguration/read|Gets a collection of disaster recovery configurations that include this server|
|/servers/disasterRecoveryConfiguration/write|Change server disaster recovery configuration|
|/servers/elasticPoolEstimates/read|Returns list of elastic pool estimates already created for this server|
|/servers/elasticPoolEstimates/write|Creates new elastic pool estimate for list of databases provided|
|/servers/elasticPools/advisors/read|Returns list of advisors available for the elastic pool|
|/servers/elasticPools/advisors/recommendedActions/read|Returns list of recommended actions of specified advisor for the elastic pool|
|/servers/elasticPools/advisors/recommendedActions/write|Apply the recommended action on the elastic pool|
|/servers/elasticPools/advisors/write|Update auto-execute status of an advisor on elastic pool level.|
|/servers/elasticPools/databases/read|Gets a list of databases for an elastic pool|
|/servers/elasticPools/delete|Delete existing elastic pool|
|/servers/elasticPools/elasticPoolActivity/read|Retrieve activities and details on a given elastic database pool|
|/servers/elasticPools/elasticPoolDatabaseActivity/read|Retrieve activities and details on a given database that is part of elastic database pool|
|/servers/elasticPools/metricDefinitions/read|Return types of metrics that are available for elastic database pools|
|/servers/elasticPools/metrics/read|Return metrics for elastic database pools|
|/servers/elasticPools/operations/cancel/action|Cancels Azure SQL elastic pool pending asynchronous operation that is not finished yet.|
|/servers/elasticPools/operations/read|Return the list of operations performed on the elastic pool|
|/servers/elasticPools/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/servers/elasticPools/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/servers/elasticPools/providers/Microsoft.Insights/metricDefinitions/read|Return types of metrics that are available for elastic database pools|
|/servers/elasticPools/read|Retrieve details of elastic pool on a given server|
|/servers/elasticPools/skus/read|Gets a collection of skus available for this elastic pool|
|/servers/elasticPools/write|Create a new or change properties of existing elastic pool|
|/servers/encryptionProtector/read|Returns a list of server encryption protectors or gets the properties for the specified server encryption protector.|
|/servers/encryptionProtector/write|Update the properties for the specified Server Encryption Protector.|
|/servers/extendedAuditingSettings/read|Retrieve details of the extended server blob auditing policy configured on a given server|
|/servers/extendedAuditingSettings/write|Change the extended server blob auditing for a given server|
|/servers/failoverGroups/delete|Deletes an existing failover group.|
|/servers/failoverGroups/failover/action|Executes planned failover in an existing failover group.|
|/servers/failoverGroups/forceFailoverAllowDataLoss/action|Executes forced failover in an existing failover group.|
|/servers/failoverGroups/read|Returns the list of failover groups or gets the properties for the specified failover group.|
|/servers/failoverGroups/write|Creates a failover group with the specified parameters or updates the properties or tags for the specified failover group.|
|/servers/firewallRules/delete|Deletes an existing server firewall rule.|
|/servers/firewallRules/read|Return the list of server firewall rules or gets the properties for the specified server firewall rule.|
|/servers/firewallRules/write|Creates a server firewall rule with the specified parameters, update the properties for the specified rule or overwrite all existing rules with new server firewall rule(s).|
|/servers/import/action|Create a new database on the server and deploy schema and data from a DacPac package|
|/servers/importExportOperationResults/read|Gets in-progress import/export operations|
|/servers/keys/delete|Deletes an existing server key.|
|/servers/keys/read|Return the list of server keys or gets the properties for the specified server key.|
|/servers/keys/write|Creates a key with the specified parameters or update the properties or tags for the specified server key.|
|/servers/operationResults/read|Gets in-progress server operations|
|/servers/providers/Microsoft.Insights/metricDefinitions/read|Return types of metrics that are available for servers|
|/servers/read|Return the list of servers or gets the properties for the specified server.|
|/servers/recommendedElasticPools/databases/read|Retrieve metrics for recommended elastic database pools for a given server|
|/servers/recommendedElasticPools/read|Retrieve recommendation for elastic database pools to reduce cost or improve performance based on historica resource utilization|
|/servers/recoverableDatabases/read|This operation is used for disaster recovery of live database to restore database to last-known good backup point. It returns information about the last good backup but it doesn\u0027t actually restore the database.|
|/servers/restorableDroppedDatabases/read|Get a list of databases that were dropped on a given server that are still within retention policy.|
|/servers/securityAlertPolicies/operationResults/read|Retrieve results of the server threat detection policy write operation|
|/servers/securityAlertPolicies/read|Retrieve details of the server threat detection policy configured on a given server|
|/servers/securityAlertPolicies/write|Change the server threat detection policy for a given server|
|/servers/serviceObjectives/read|Retrieve list of service level objectives (also known as performance tiers) available on a given server|
|/servers/syncAgents/delete|Deletes an existing sync agent.|
|/servers/syncAgents/generateKey/action|Generate sync agent registeration key|
|/servers/syncAgents/linkedDatabases/read|Return the list of sync agent linked databases|
|/servers/syncAgents/read|Return the list of sync agents or gets the properties for the specified sync agent.|
|/servers/syncAgents/write|Creates a sync agent with the specified parameters or update the properties for the specified sync agent.|
|/servers/usages/read|Return server DTU quota and current DTU consuption by all databases within the server|
|/servers/virtualNetworkRules/delete|Deletes an existing Virtual Network Rule|
|/servers/virtualNetworkRules/read|Return the list of virtual network rules or gets the properties for the specified virtual network rule.|
|/servers/virtualNetworkRules/write|Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule.|
|/servers/write|Creates a server with the specified parameters or update the properties or tags for the specified server.|
|/unregister/action|UnRegisters the subscription for the Microsoft SQL Database resource provider and enables the creation of Microsoft SQL Databases.|
|/virtualClusters/read|Return the list of virtual clusters or gets the properties for the specified virtual cluster.|
|/virtualClusters/write|Updates virtual cluster tags.|

## <a name="microsoftstorage"></a>Microsoft.Storage

| Operation | Description |
|---|---|
|/checknameavailability/read|Checks that account name is valid and is not in use.|
|/locations/deleteVirtualNetworkOrSubnets/action|Notifies Microsoft.Storage that virtual network or subnet is being deleted|
|/operations/read|Polls the status of an asynchronous operation.|
|/register/action|Registers the subscription for the storage resource provider and enables the creation of storage accounts.|
|/skus/read|Lists the Skus supported by Microsoft.Storage.|
|/storageAccounts/blobServices/containers/clearLegalHold/action|Clear blob container legal hold|
|/storageAccounts/blobServices/containers/delete|Returns the result of deleting a container|
|/storageAccounts/blobServices/containers/immutabilityPolicies/delete|Delete blob container immutability policy|
|/storageAccounts/blobServices/containers/immutabilityPolicies/extend/action|Extend blob container immutability policy|
|/storageAccounts/blobServices/containers/immutabilityPolicies/lock/action|Lock blob container immutability policy|
|/storageAccounts/blobServices/containers/immutabilityPolicies/read|Get blob container immutability policy|
|/storageAccounts/blobServices/containers/immutabilityPolicies/write|Put blob container immutability policy|
|/storageAccounts/blobServices/containers/read|Returns a container or a list of containers|
|/storageAccounts/blobServices/containers/setLegalHold/action|Set blob container legal hold|
|/storageAccounts/blobServices/containers/write|Returns the result of put or lease blob container|
|/storageAccounts/blobServices/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource.|
|/storageAccounts/blobServices/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource.|
|/storageAccounts/blobServices/providers/Microsoft.Insights/metricDefinitions/read|Get list of Microsoft Storage Metrics definitions.|
|/storageAccounts/blobServices/read|Returns blob service properties or statistics|
|/storageAccounts/blobServices/write|Returns the result of put blob service properties|
|/storageAccounts/delete|Deletes an existing storage account.|
|/storageAccounts/fileServices/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource.|
|/storageAccounts/fileServices/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource.|
|/storageAccounts/fileServices/providers/Microsoft.Insights/metricDefinitions/read|Get list of Microsoft Storage Metrics definitions.|
|/storageAccounts/listAccountSas/action|Returns the Account SAS token for the specified storage account.|
|/storageAccounts/listkeys/action|Returns the access keys for the specified storage account.|
|/storageAccounts/listServiceSas/action|Returns the Service SAS token for the specified storage account.|
|/storageAccounts/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource.|
|/storageAccounts/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource.|
|/storageAccounts/providers/Microsoft.Insights/metricDefinitions/read|Get list of Microsoft Storage Metrics definitions.|
|/storageAccounts/queueServices/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource.|
|/storageAccounts/queueServices/providers/Microsoft.Insights/metricDefinitions/read|Get list of Microsoft Storage Metrics definitions.|
|/storageAccounts/queueServices/queues/delete|Returns the result of deleting a queue|
|/storageAccounts/queueServices/queues/read|Returns a queue or a list of queues.|
|/storageAccounts/queueServices/queues/write|Returns the result of writing a queue|
|/storageAccounts/queueServices/read|Returns queue service properties or statistics.|
|/storageAccounts/queueServices/write|Returns the result of setting queue service properties|
|/storageAccounts/read|Returns the list of storage accounts or gets the properties for the specified storage account.|
|/storageAccounts/regeneratekey/action|Regenerates the access keys for the specified storage account.|
|/storageAccounts/services/diagnosticSettings/write|Create/Update storage account diagnostic settings.|
|/storageAccounts/storageAccounts/queueServices/providers/ Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource.|
|/storageAccounts/tableServices/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource.|
|/storageAccounts/tableServices/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource.|
|/storageAccounts/tableServices/providers/Microsoft.Insights/metricDefinitions/read|Get list of Microsoft Storage Metrics definitions.|
|/storageAccounts/write|Creates a storage account with the specified parameters or update the properties or tags or adds custom domain for the specified storage account.|
|/usages/read|Returns the limit and the current usage count for resources in the specified subscription|

## <a name="microsoftstoragesync"></a>Microsoft.StorageSync

| Operation | Description |
|---|---|
|/storageSyncServices/delete|Delete any Storage Sync Services|
|/storageSyncServices/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for Storage Sync Services|
|/storageSyncServices/read|Read any Storage Sync Services|
|/storageSyncServices/registeredServers/delete|Delete any Registered Server|
|/storageSyncServices/registeredServers/read|Read any Registered Server|
|/storageSyncServices/registeredServers/write|Create or Update any Registered Server|
|/storageSyncServices/syncGroups/cloudEndpoints/delete|Delete any Cloud Endpoints|
|/storageSyncServices/syncGroups/cloudEndpoints/operationresults/read|Location api for async backup calls|
|/storageSyncServices/syncGroups/cloudEndpoints/postbackup/action|Call this action after backup|
|/storageSyncServices/syncGroups/cloudEndpoints/postrestore/action|Call this action after restore|
|/storageSyncServices/syncGroups/cloudEndpoints/prebackup/action|Call this action before backup|
|/storageSyncServices/syncGroups/cloudEndpoints/prerestore/action|Call this action before restore|
|/storageSyncServices/syncGroups/cloudEndpoints/read|Read any Cloud Endpoints|
|/storageSyncServices/syncGroups/cloudEndpoints/restoreheartbeat/action|Restore heartbeat|
|/storageSyncServices/syncGroups/cloudEndpoints/write|Create or Update any Cloud Endpoints|
|/storageSyncServices/syncGroups/delete|Delete any Sync Groups|
|/storageSyncServices/syncGroups/read|Read any Sync Groups|
|/storageSyncServices/syncGroups/serverEndpoints/delete|Delete any Server Endpoints|
|/storageSyncServices/syncGroups/serverEndpoints/read|Read any Server Endpoints|
|/storageSyncServices/syncGroups/serverEndpoints/recallAction/action|Call this action to recall files to a server|
|/storageSyncServices/syncGroups/serverEndpoints/write|Create or Update any Server Endpoints|
|/storageSyncServices/syncGroups/write|Create or Update any Sync Groups|
|/storageSyncServices/write|Create or Update any Storage Sync Services|

## <a name="microsoftstorsimple"></a>Microsoft.StorSimple

| Operation | Description |
|---|---|
|/managers/accessControlRecords/delete|Deletes the Access Control Records|
|/managers/accessControlRecords/read|Lists or gets the Access Control Records|
|/managers/accessControlRecords/write|Create or update the Access Control Records|
|/managers/alerts/read|Lists or gets the Alerts|
|/managers/bandwidthSettings/delete|Deletes an existing Bandwidth Settings (8000 Series Only)|
|/managers/bandwidthSettings/read|List the Bandwidth Settings (8000 Series Only)|
|/managers/bandwidthSettings/write|Creates a new or updates Bandwidth Settings (8000 Series Only)|
|/Managers/certificates/write|The Update Resource Certificate operation updates the resource/vault credential certificate.|
|/managers/clearAlerts/action|Clear all the alerts associated with the device manager.|
|/managers/cloudApplianceConfigurations/read|List the Cloud Appliance Supported Configurations|
|/managers/configureDevice/action|Configures a device|
|/managers/delete|Deletes the Device Managers|
|/Managers/delete|The Delete Vault operation deletes the specified Azure resource of type 'vault'|
|/managers/devices/alertSettings/read|Lists or gets the Alert Settings|
|/managers/devices/alertSettings/write|Create or update the Alert Settings|
|/managers/devices/backupPolicies/backup/action|Take a manual backup to create an on-demand backup of all the volumes protected by the policy.|
|/managers/devices/backupPolicies/delete|Deletes an existing Backup Polices (8000 Series Only)|
|/managers/devices/backupPolicies/read|List the Backup Polices (8000 Series Only)|
|/managers/devices/backupPolicies/schedules/delete|Deletes an existing Schedules|
|/managers/devices/backupPolicies/schedules/read|List the Schedules|
|/managers/devices/backupPolicies/schedules/write|Creates a new or updates Schedules|
|/managers/devices/backupPolicies/write|Creates a new or updates Backup Polices (8000 Series Only)|
|/managers/devices/backups/delete|Deletes the Backup Set|
|/managers/devices/backups/elements/clone/action|Clone a share or volume using a backup element.|
|/managers/devices/backups/read|Lists or gets the Backup Set|
|/managers/devices/backups/restore/action|Restore all the volumes from a backup set.|
|/managers/devices/backupScheduleGroups/delete|Deletes the Backup Schedule Groups|
|/managers/devices/backupScheduleGroups/read|Lists or gets the Backup Schedule Groups|
|/managers/devices/backupScheduleGroups/write|Create or update the Backup Schedule Groups|
|/managers/devices/chapSettings/delete|Deletes the Chap Settings|
|/managers/devices/chapSettings/read|Lists or gets the Chap Settings|
|/managers/devices/chapSettings/write|Create or update the Chap Settings|
|/managers/devices/deactivate/action|Deactivates a device.|
|/managers/devices/delete|Deletes the Devices|
|/managers/devices/download/action|Dowload updates for a device.|
|/managers/devices/failover/action|Failover of the device.|
|/managers/devices/fileservers/backup/action|Take backup of an File Server.|
|/managers/devices/fileservers/delete|Deletes the File Servers|
|/managers/devices/fileservers/metrics/read|Lists or gets the Metrics|
|/managers/devices/fileservers/metricsDefinitions/read|Lists or gets the Metrics Definitions|
|/managers/devices/fileservers/read|Lists or gets the File Servers|
|/managers/devices/fileservers/shares/delete|Deletes the Shares|
|/managers/devices/fileservers/shares/metrics/read|Lists or gets the Metrics|
|/managers/devices/fileservers/shares/metricsDefinitions/read|Lists or gets the Metrics Definitions|
|/managers/devices/fileservers/shares/read|Lists or gets the Shares|
|/managers/devices/fileservers/shares/write|Create or update the Shares|
|/managers/devices/fileservers/write|Create or update the File Servers|
|/managers/devices/hardwareComponentGroups/changeControllerPowerState/action|Change controller power state of hardware component groups|
|/managers/devices/hardwareComponentGroups/read|List the Hardware Component Groups|
|/managers/devices/install/action|Install updates on a device.|
|/managers/devices/installUpdates/action|Installs updates on the devices|
|/managers/devices/iscsiservers/backup/action|Take backup of an iSCSI server.|
|/managers/devices/iscsiservers/delete|Deletes the iSCSI Servers|
|/managers/devices/iscsiservers/disks/delete|Deletes the Disks|
|/managers/devices/iscsiservers/disks/metrics/read|Lists or gets the Metrics|
|/managers/devices/iscsiservers/disks/metricsDefinitions/read|Lists or gets the Metrics Definitions|
|/managers/devices/iscsiservers/disks/read|Lists or gets the Disks|
|/managers/devices/iscsiservers/disks/write|Create or update the Disks|
|/managers/devices/iscsiservers/metrics/read|Lists or gets the Metrics|
|/managers/devices/iscsiservers/metricsDefinitions/read|Lists or gets the Metrics Definitions|
|/managers/devices/iscsiservers/read|Lists or gets the iSCSI Servers|
|/managers/devices/iscsiservers/write|Create or update the iSCSI Servers|
|/managers/devices/jobs/cancel/action|Cancel a running job|
|/managers/devices/jobs/read|Lists or gets the Jobs|
|/managers/devices/listFailoverSets/action|List the failover sets for an existing device.|
|/managers/devices/listFailoverTargets/action|List failover targets of the devices|
|/managers/devices/metrics/read|Lists or gets the Metrics|
|/managers/devices/metricsDefinitions/read|Lists or gets the Metrics Definitions|
|/managers/devices/migrationSourceConfigurations/confirmMigration/action|Confirms a successful migration and commit it.|
|/managers/devices/migrationSourceConfigurations/fetchConfirmMigrationStatus/action|Fetch the confirm status of migration.|
|/managers/devices/migrationSourceConfigurations/fetchMigrationEstimate/action|Fetch the status for the migration estimation job.|
|/managers/devices/migrationSourceConfigurations/fetchMigrationStatus/action|Fetch the status for the migration.|
|/managers/devices/migrationSourceConfigurations/import/action|Import source configurations for migration|
|/managers/devices/migrationSourceConfigurations/startMigration/action|Start migration using source configurations|
|/managers/devices/migrationSourceConfigurations/startMigrationEstimate/action|Start a job to estimate the duration of the migration process.|
|/managers/devices/networkSettings/read|Lists or gets the Network Settings|
|/managers/devices/networkSettings/write|Creates a new or updates Network Settings|
|/managers/devices/publicEncryptionKey/action|List public encryption key of the device manager|
|/managers/devices/publishSupportPackage/action|Publish support package of a device for Microsoft Support troubleshooting.|
|/managers/devices/read|Lists or gets the Devices|
|/managers/devices/scanForUpdates/action|Scan for updates in a device.|
|/managers/devices/securitySettings/read|List the Security Settings|
|/managers/devices/securitySettings/syncRemoteManagementCertificate/action|Synchronize the remote management certificate for a device.|
|/managers/devices/securitySettings/update/action|Update the security settings.|
|/managers/devices/securitySettings/write|Creates a new or updates Security Settings|
|/managers/devices/sendTestAlertEmail/action|Send test alert email to configured email recipients.|
|/managers/devices/timeSettings/read|Lists or gets the Time Settings|
|/managers/devices/timeSettings/write|Creates a new or updates Time Settings|
|/managers/devices/updateSummary/read|Lists or gets the Update Summary|
|/managers/devices/volumeContainers/delete|Deletes an existing Volume Containers (8000 Series Only)|
|/managers/devices/volumeContainers/listEncryptionKeys/action|List encryption keys of Volume Containers|
|/managers/devices/volumeContainers/metrics/read|List the Metrics|
|/managers/devices/volumeContainers/metricsDefinitions/read|List the Metrics Definitions|
|/managers/devices/volumeContainers/read|List the Volume Containers (8000 Series Only)|
|/managers/devices/volumeContainers/rolloverEncryptionKey/action|Rollover encryption keys of Volume Containers|
|/managers/devices/volumeContainers/volumes/delete|Deletes an existing Volumes|
|/managers/devices/volumeContainers/volumes/metrics/read|List the Metrics|
|/managers/devices/volumeContainers/volumes/metricsDefinitions/read|List the Metrics Definitions|
|/managers/devices/volumeContainers/volumes/read|List the Volumes|
|/managers/devices/volumeContainers/volumes/write|Creates a new or updates Volumes|
|/managers/devices/volumeContainers/write|Creates a new or updates Volume Containers (8000 Series Only)|
|/managers/devices/write|Create or update the Devices|
|/managers/encryptionSettings/read|Lists or gets the Encryption Settings|
|/Managers/extendedInformation/delete|The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault?|
|/Managers/extendedInformation/read|The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault?|
|/Managers/extendedInformation/write|The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault?|
|/managers/getActivationKey/action|Get activation key for the device manager.|
|/managers/getEncryptionKey/action|Get encryption key for the device manager.|
|/managers/listActivationKey/action|Gets the activation key of the StorSimple Device Manager.|
|/managers/listPrivateEncryptionKey/action|Gets private encryption key for a StorSimple Device Manager.|
|/managers/listPublicEncryptionKey/action|List public encryption keys of a StorSimple Device Manager.|
|/managers/metrics/read|Lists or gets the Metrics|
|/managers/metricsDefinitions/read|Lists or gets the Metrics Definitions|
|/managers/provisionCloudAppliance/action|Create a new cloud appliance.|
|/managers/read|Lists or gets the Device Managers|
|/Managers/read|The Get Vault operation gets an object representing the Azure resource of type 'vault'|
|/managers/regenarateRegistationCertificate/action|Regenerate registration certificate for the device managers.|
|/managers/regenerateActivationKey/action|Regenerate activation key for the device manager.|
|/managers/storageAccountCredentials/delete|Deletes the Storage Account Credentials|
|/managers/storageAccountCredentials/listAccessKey/action|List access keys of Storage Account Credentials|
|/managers/storageAccountCredentials/read|Lists or gets the Storage Account Credentials|
|/managers/storageAccountCredentials/write|Create or update the Storage Account Credentials|
|/managers/storageDomains/delete|Deletes the Storage Domains|
|/managers/storageDomains/read|Lists or gets the Storage Domains|
|/managers/storageDomains/write|Create or update the Storage Domains|
|/managers/write|Create or update the Device Managers|
|/Managers/write|Create Vault operation creates an Azure resource of type 'vault'|

## <a name="microsoftstreamanalytics"></a>Microsoft.StreamAnalytics

| Operation | Description |
|---|---|
|/locations/quotas/Read|Read Stream Analytics Subscription Quota|
|/operations/Read|Read Stream Analytics Operations|
|/Register/action|Register subscription with Stream Analytics Resource Provider|
|/streamingjobs/Delete|Delete Stream Analytics Job|
|/streamingjobs/functions/Delete|Delete Stream Analytics Job Function|
|/streamingjobs/functions/operationresults/Read|Read operation results for Stream Analytics Job Function|
|/streamingjobs/functions/Read|Read Stream Analytics Job Function|
|/streamingjobs/functions/RetrieveDefaultDefinition/action|Retrieve Default Definition of a Stream Analytics Job Function|
|/streamingjobs/functions/Test/action|Test Stream Analytics Job Function|
|/streamingjobs/functions/Write|Write Stream Analytics Job Function|
|/streamingjobs/inputs/Delete|Delete Stream Analytics Job Input|
|/streamingjobs/inputs/operationresults/Read|Read operation results for Stream Analytics Job Input|
|/streamingjobs/inputs/Read|Read Stream Analytics Job Input|
|/streamingjobs/inputs/Sample/action|Sample Stream Analytics Job Input|
|/streamingjobs/inputs/Test/action|Test Stream Analytics Job Input|
|/streamingjobs/inputs/Write|Write Stream Analytics Job Input|
|/streamingjobs/metricdefinitions/Read|Read Metric Definitions|
|/streamingjobs/operationresults/Read|Read operation results for Stream Analytics Job|
|/streamingjobs/outputs/Delete|Delete Stream Analytics Job Output|
|/streamingjobs/outputs/operationresults/Read|Read operation results for Stream Analytics Job Output|
|/streamingjobs/outputs/Read|Read Stream Analytics Job Output|
|/streamingjobs/outputs/Test/action|Test Stream Analytics Job Output|
|/streamingjobs/outputs/Write|Write Stream Analytics Job Output|
|/streamingjobs/providers/Microsoft.Insights/diagnosticSettings/read|Read diagnostic setting.|
|/streamingjobs/providers/Microsoft.Insights/diagnosticSettings/write|Write diagnostic setting.|
|/streamingjobs/providers/Microsoft.Insights/logDefinitions/read|Gets the available logs for streamingjobs|
|/streamingjobs/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for streamingjobs|
|/streamingjobs/Read|Read Stream Analytics Job|
|/streamingjobs/Start/action|Start Stream Analytics Job|
|/streamingjobs/Stop/action|Stop Stream Analytics Job|
|/streamingjobs/transformations/Delete|Delete Stream Analytics Job Transformation|
|/streamingjobs/transformations/Read|Read Stream Analytics Job Transformation|
|/streamingjobs/transformations/Write|Write Stream Analytics Job Transformation|
|/streamingjobs/Write|Write Stream Analytics Job|

## <a name="microsoftsubscription"></a>Microsoft.Subscription

| Operation | Description |
|---|---|
|/SubscriptionDefinitions/read|Get an Azure subscription definition within a management group.|
|/SubscriptionDefinitions/write|Create an Azure subscription definition|

## <a name="microsoftsupport"></a>Microsoft.Support

| Operation | Description |
|---|---|
|/register/action|Registers to Support Resource Provider|
|/supportTickets/read|Gets Support Ticket details (including status, severity, contact details and communications) or gets the list of Support Tickets across subscriptions.|
|/supportTickets/write|Creates or Updates a Support Ticket. You can create a Support Ticket for Technical, Billing, Quotas or Subscription Management related issues. You can update severity, contact details and communications for existing support tickets.|

## <a name="microsofttimeseriesinsights"></a>Microsoft.TimeSeriesInsights

| Operation | Description |
|---|---|
|/environments/accesspolicies/delete|Deletes the access policy.|
|/environments/accesspolicies/read|Get the properties of an access policy.|
|/environments/accesspolicies/write|Creates a new access policy for an environment, or updates an existing access policy.|
|/environments/delete|Deletes the environment.|
|/environments/eventsources/delete|Deletes the event source.|
|/environments/eventsources/eventsources/providers/Microsoft.Insights/ diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/environments/eventsources/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/environments/eventsources/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for eventsources|
|/environments/eventsources/read|Get the properties of an event source.|
|/environments/eventsources/write|Creates a new event source for an environment, or updates an existing event source.|
|/environments/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/environments/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/environments/providers/Microsoft.Insights/metricDefinitions/read|Gets the available metrics for environments|
|/environments/read|Get the properties of an environment.|
|/environments/referencedatasets/delete|Deletes the reference data set.|
|/environments/referencedatasets/read|Get the properties of a reference data set.|
|/environments/referencedatasets/write|Creates a new reference data set for an environment, or updates an existing reference data set.|
|/environments/status/read|Get the status of the environment, state of its associated operations like ingress.|
|/environments/write|Creates a new environment, or updates an existing environment.|
|/register/action|Registers the subscription for the Time Series Insights resource provider and enables the creation of Time Series Insights environments.|

## <a name="microsoftweb"></a>microsoft.web

| Operation | Description |
|---|---|
|/apimanagementaccounts/apiacls/read|Get Api Management Accounts Apiacls.|
|/apimanagementaccounts/apis/apiacls/delete|Delete Api Management Accounts APIs Apiacls.|
|/apimanagementaccounts/apis/apiacls/read|Get Api Management Accounts APIs Apiacls.|
|/apimanagementaccounts/apis/apiacls/write|Update Api Management Accounts APIs Apiacls.|
|/apimanagementaccounts/apis/connectionacls/read|Get Api Management Accounts APIs Connectionacls.|
|/apimanagementaccounts/apis/connections/confirmconsentcode/action|Confirm Consent Code Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/connections/connectionacls/delete|Delete Api Management Accounts APIs Connections Connectionacls.|
|/apimanagementaccounts/apis/connections/connectionacls/read|Get Api Management Accounts APIs Connections Connectionacls.|
|/apimanagementaccounts/apis/connections/connectionacls/write|Update Api Management Accounts APIs Connections Connectionacls.|
|/apimanagementaccounts/apis/connections/delete|Delete Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/connections/getconsentlinks/action|Get Consent Links for Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/connections/listconnectionkeys/action|List Connection Keys Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/connections/listsecrets/action|List Secrets Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/connections/read|Get Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/connections/write|Update Api Management Accounts APIs Connections.|
|/apimanagementaccounts/apis/delete|Delete Api Management Accounts APIs.|
|/apimanagementaccounts/apis/localizeddefinitions/delete|Delete Api Management Accounts APIs Localized Definitions.|
|/apimanagementaccounts/apis/localizeddefinitions/read|Get Api Management Accounts APIs Localized Definitions.|
|/apimanagementaccounts/apis/localizeddefinitions/write|Update Api Management Accounts APIs Localized Definitions.|
|/apimanagementaccounts/apis/read|Get Api Management Accounts APIs.|
|/apimanagementaccounts/apis/write|Update Api Management Accounts APIs.|
|/apimanagementaccounts/connectionacls/read|Get Api Management Accounts Connectionacls.|
|/availablestacks/read|Get Available Stacks.|
|/billingmeters/read|Get list of billing meters.|
|/certificates/Delete|Delete an existing certificate.|
|/certificates/Read|Get the list of certificates.|
|/certificates/Write|Add a new certificate or update an existing one.|
|/checknameavailability/read|Check if resource name is available.|
|/classicmobileservices/read|Get Classic Mobile Services.|
|/connectionGateways/Delete|Deletes a Connection Gateway.|
|/connectionGateways/Join/Action|Joins a Connection Gateway.|
|/connectiongateways/liststatus/action|List Status Connection Gateways.|
|/connectionGateways/ListStatus/Action|Lists status of a Connection Gateway.|
|/connectionGateways/Move/Action|Moves a Connection Gateway.|
|/connectionGateways/Read|Get the list of Connection Gateways.|
|/connectionGateways/Write|Creates or updates a Connection Gateway.|
|/connections/confirmconsentcode/action|Confirm Connections Consent Code.|
|/connections/Delete|Deletes a Connection.|
|/connections/Join/Action|Joins a Connection.|
|/connections/listconsentlinks/action|List Consent Links for Connections.|
|/connections/Move/Action|Moves a Connection.|
|/connections/Read|Get the list of Connections.|
|/connections/Write|Creates or updates a Connection.|
|/customApis/Delete|Deletes a Custom API.|
|/customApis/extractApiDefinitionFromWsdl/Action|Extracts API definition from a WSDL.|
|/customApis/Join/Action|Joins a Custom API.|
|/customApis/listWsdlInterfaces/Action|Lists WSDL interfaces for a Custom API.|
|/customApis/Move/Action|Moves a Custom API.|
|/customApis/Read|Get the list of Custom API.|
|/customApis/Write|Creates or updates a Custom API.|
|/deploymentlocations/read|Get Deployment Locations.|
|/geoRegions/Read|Get the list of Geo regions.|
|/hostingenvironments/capacities/read|Get Hosting Environments Capacities.|
|/hostingEnvironments/Delete|Delete an App Service Environment|
|/hostingenvironments/diagnostics/read|Get Hosting Environments Diagnostics.|
|/hostingenvironments/inboundnetworkdependenciesendpoints/read|Get the network endpoints of all inbound dependencies.|
|/hostingenvironments/metricdefinitions/read|Get Hosting Environments Metric Definitions.|
|/hostingenvironments/multirolepools/metricdefinitions/read|Get Hosting Environments MultiRole Pools Metric Definitions.|
|/hostingenvironments/multirolepools/metrics/read|Get Hosting Environments MultiRole Pools Metrics.|
|/hostingEnvironments/multiRolePools/providers/Microsoft.Insights/ metricDefinitions/Read|Gets the available metrics for App Service Environment MultiRole|
|/hostingEnvironments/multiRolePools/Read|Get the properties of a FrontEnd Pool in an App Service Environment|
|/hostingenvironments/multirolepools/skus/read|Get Hosting Environments MultiRole Pools SKUs.|
|/hostingenvironments/multirolepools/usages/read|Get Hosting Environments MultiRole Pools Usages.|
|/hostingEnvironments/multiRolePools/Write|Create a new FrontEnd Pool in an App Service Environment or update an existing one|
|/hostingenvironments/operations/read|Get Hosting Environments Operations.|
|/hostingenvironments/outboundnetworkdependenciesendpoints/read|Get the network endpoints of all outbound dependencies.|
|/hostingenvironments/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/hostingenvironments/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/hostingEnvironments/Read|Get the properties of an App Service Environment|
|/hostingEnvironments/reboot/Action|Reboot all machines in an App Service Environment|
|/hostingenvironments/resume/action|Resume Hosting Environments.|
|/hostingenvironments/serverfarms/read|Get Hosting Environments App Service Plans.|
|/hostingenvironments/sites/read|Get Hosting Environments Web Apps.|
|/hostingenvironments/suspend/action|Suspend Hosting Environments.|
|/hostingenvironments/usages/read|Get Hosting Environments Usages.|
|/hostingenvironments/workerpools/metricdefinitions/read|Get Hosting Environments Workerpools Metric Definitions.|
|/hostingenvironments/workerpools/metrics/read|Get Hosting Environments Workerpools Metrics.|
|/hostingEnvironments/workerPools/providers/Microsoft.Insights/metricDefinitions/Read|Gets the available metrics for App Service Environment WorkerPool|
|/hostingEnvironments/workerPools/Read|Get the properties of a Worker Pool in an App Service Environment|
|/hostingenvironments/workerpools/skus/read|Get Hosting Environments Workerpools SKUs.|
|/hostingenvironments/workerpools/usages/read|Get Hosting Environments Workerpools Usages.|
|/hostingEnvironments/workerPools/Write|Create a new Worker Pool in an App Service Environment or update an existing one|
|/hostingEnvironments/Write|Create a new App Service Environment or update existing one|
|/ishostingenvironmentnameavailable/read|Get if Hosting Environment Name is available.|
|/ishostnameavailable/read|Check if Hostname is Available.|
|/isusernameavailable/read|Check if Username is available.|
|/listSitesAssignedToHostName/Read|Get names of sites assigned to hostname.|
|/locations/apioperations/read|Get Locations API Operations.|
|/locations/connectiongatewayinstallations/read|Get Locations Connection Gateway Installations.|
|/locations/extractapidefinitionfromwsdl/action|Extract Api Definition from WSDL for Locations.|
|/locations/listwsdlinterfaces/action|List WSDL Interfaces for Locations.|
|/locations/managedapis/apioperations/read|Get Locations Managed API Operations.|
|/locations/managedapis/Join/Action|Joins a Managed API.|
|/locations/managedapis/read|Get Locations Managed APIs.|
|/operations/read|Get Operations.|
|/publishingusers/read|Get Publishing Users.|
|/publishingusers/write|Update Publishing Users.|
|/recommendations/Read|Get the list of recommendations for subscriptions.|
|/register/action|Register Microsoft.Web resource provider for the subscription.|
|/resourcehealthmetadata/read|Get Resource Health Metadata.|
|/serverfarms/capabilities/read|Get App Service Plans Capabilities.|
|/serverfarms/Delete|Delete an existing App Service Plan|
|/serverfarms/firstpartyapps/settings/delete|Delete App Service Plans First Party Apps Settings.|
|/serverfarms/firstpartyapps/settings/read|Get App Service Plans First Party Apps Settings.|
|/serverfarms/firstpartyapps/settings/write|Update App Service Plans First Party Apps Settings.|
|/serverfarms/hybridconnectionnamespaces/relays/delete|Delete App Service Plans Hybrid Connection Namespaces Relays.|
|/serverfarms/hybridconnectionnamespaces/relays/read|Get App Service Plans Hybrid Connection Namespaces Relays.|
|/serverfarms/hybridconnectionnamespaces/relays/sites/read|Get App Service Plans Hybrid Connection Namespaces Relays Web Apps.|
|/serverfarms/hybridconnectionplanlimits/read|Get App Service Plans Hybrid Connection Plan Limits.|
|/serverfarms/hybridconnectionrelays/read|Get App Service Plans Hybrid Connection Relays.|
|/serverfarms/metricdefinitions/read|Get App Service Plans Metric Definitions.|
|/serverfarms/metrics/read|Get App Service Plans Metrics.|
|/serverfarms/operationresults/read|Get App Service Plans Operation Results.|
|/serverfarms/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/serverfarms/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/serverfarms/providers/Microsoft.Insights/metricDefinitions/Read|Gets the available metrics for App Service Plan|
|/serverfarms/Read|Get the properties on an App Service Plan|
|/serverfarms/restartSites/Action|Restart all Web Apps in an App Service Plan|
|/serverfarms/sites/read|Get App Service Plans Web Apps.|
|/serverfarms/skus/read|Get App Service Plans SKUs.|
|/serverfarms/usages/read|Get App Service Plans Usages.|
|/serverfarms/virtualnetworkconnections/gateways/write|Update App Service Plans Virtual Network Connections Gateways.|
|/serverfarms/virtualnetworkconnections/read|Get App Service Plans Virtual Network Connections.|
|/serverfarms/virtualnetworkconnections/routes/delete|Delete App Service Plans Virtual Network Connections Routes.|
|/serverfarms/virtualnetworkconnections/routes/read|Get App Service Plans Virtual Network Connections Routes.|
|/serverfarms/virtualnetworkconnections/routes/write|Update App Service Plans Virtual Network Connections Routes.|
|/serverfarms/workers/reboot/action|Reboot App Service Plans Workers.|
|/serverfarms/Write|Create a new App Service Plan or update an existing one|
|/sites/analyzecustomhostname/read|Analyze Custom Hostname.|
|/sites/applySlotConfig/Action|Apply web app slot configuration from target slot to the current web app|
|/sites/backup/Action|Create a new web app backup|
|/sites/backup/read|Get Web Apps Backup.|
|/sites/backup/write|Update Web Apps Backup.|
|/sites/backups/delete|Delete Web Apps Backups.|
|/sites/backups/list/action|List Web Apps Backups.|
|/sites/backups/Read|Get the properties of a web app's backup|
|/sites/backups/restore/action|Restore Web Apps Backups.|
|/sites/config/delete|Delete Web Apps Config.|
|/sites/config/list/Action|List Web App's security sensitive settings, such as publishing credentials, app settings and connection strings|
|/sites/config/Read|Get Web App configuration settings|
|/sites/config/Write|Update Web App's configuration settings|
|/sites/continuouswebjobs/delete|Delete Web Apps Continuous Web Jobs.|
|/sites/continuouswebjobs/read|Get Web Apps Continuous Web Jobs.|
|/sites/continuouswebjobs/start/action|Start Web Apps Continuous Web Jobs.|
|/sites/continuouswebjobs/stop/action|Stop Web Apps Continuous Web Jobs.|
|/sites/Delete|Delete an existing Web App|
|/sites/deployments/delete|Delete Web Apps Deployments.|
|/sites/deployments/log/read|Get Web Apps Deployments Log.|
|/sites/deployments/read|Get Web Apps Deployments.|
|/sites/deployments/write|Update Web Apps Deployments.|
|/sites/diagnostics/analyses/execute/Action|Run Web Apps Diagnostics Analysis.|
|/sites/diagnostics/analyses/read|Get Web Apps Diagnostics Analysis.|
|/sites/diagnostics/aspnetcore/read|Get Web Apps Diagnostics for ASP.NET Core app.|
|/sites/diagnostics/autoheal/read|Get Web Apps Diagnostics Autoheal.|
|/sites/diagnostics/deployment/read|Get Web Apps Diagnostics Deployment.|
|/sites/diagnostics/deployments/read|Get Web Apps Diagnostics Deployments.|
|/sites/diagnostics/detectors/execute/Action|Run Web Apps Diagnostics Detector.|
|/sites/diagnostics/detectors/read|Get Web Apps Diagnostics Detector.|
|/sites/diagnostics/failedrequestsperuri/read|Get Web Apps Diagnostics Failed Requests Per Uri.|
|/sites/diagnostics/frebanalysis/read|Get Web Apps Diagnostics FREB Analysis.|
|/sites/diagnostics/loganalyzer/read|Get Web Apps Diagnostics Log Analyzer.|
|/sites/diagnostics/read|Get Web Apps Diagnostics Categories.|
|/sites/diagnostics/runtimeavailability/read|Get Web Apps Diagnostics Runtime Availability.|
|/sites/diagnostics/servicehealth/read|Get Web Apps Diagnostics Service Health.|
|/sites/diagnostics/sitecpuanalysis/read|Get Web Apps Diagnostics Site CPU Analysis.|
|/sites/diagnostics/sitecrashes/read|Get Web Apps Diagnostics Site Crashes.|
|/sites/diagnostics/sitelatency/read|Get Web Apps Diagnostics Site Latency.|
|/sites/diagnostics/sitememoryanalysis/read|Get Web Apps Diagnostics Site Memory Analysis.|
|/sites/diagnostics/siterestartsettingupdate/read|Get Web Apps Diagnostics Site Restart Setting Update.|
|/sites/diagnostics/siterestartuserinitiated/read|Get Web Apps Diagnostics Site Restart User Initiated.|
|/sites/diagnostics/siteswap/read|Get Web Apps Diagnostics Site Swap.|
|/sites/diagnostics/threadcount/read|Get Web Apps Diagnostics Thread Count.|
|/sites/diagnostics/workeravailability/read|Get Web Apps Diagnostics Workeravailability.|
|/sites/diagnostics/workerprocessrecycle/read|Get Web Apps Diagnostics Worker Process Recycle.|
|/sites/domainownershipidentifiers/read|Get Web Apps Domain Ownership Identifiers.|
|/sites/domainownershipidentifiers/write|Update Web Apps Domain Ownership Identifiers.|
|/sites/functions/action|Functions Web Apps.|
|/sites/functions/delete|Delete Web Apps Functions.|
|/sites/functions/listsecrets/action|List Secrets Web Apps Functions.|
|/sites/functions/masterkey/read|Get Web Apps Functions Masterkey.|
|/sites/functions/read|Get Web Apps Functions.|
|/sites/functions/token/read|Get Web Apps Functions Token.|
|/sites/functions/write|Update Web Apps Functions.|
|/sites/hostnamebindings/delete|Delete Web Apps Hostname Bindings.|
|/sites/hostnamebindings/read|Get Web Apps Hostname Bindings.|
|/sites/hostnamebindings/write|Update Web Apps Hostname Bindings.|
|/sites/hybridconnection/delete|Delete Web Apps Hybrid Connection.|
|/sites/hybridconnection/read|Get Web Apps Hybrid Connection.|
|/sites/hybridconnection/write|Update Web Apps Hybrid Connection.|
|/sites/hybridconnectionnamespaces/relays/delete|Delete Web Apps Hybrid Connection Namespaces Relays.|
|/sites/hybridconnectionnamespaces/relays/listkeys/action|List Keys Web Apps Hybrid Connection Namespaces Relays.|
|/sites/hybridconnectionnamespaces/relays/read|Get Web Apps Hybrid Connection Namespaces Relays.|
|/sites/hybridconnectionnamespaces/relays/write|Update Web Apps Hybrid Connection Namespaces Relays.|
|/sites/hybridconnectionrelays/read|Get Web Apps Hybrid Connection Relays.|
|/sites/instances/deployments/delete|Delete Web Apps Instances Deployments.|
|/sites/instances/deployments/read|Get Web Apps Instances Deployments.|
|/sites/instances/extensions/log/read|Get Web Apps Instances Extensions Log.|
|/sites/instances/extensions/read|Get Web Apps Instances Extensions.|
|/sites/instances/processes/delete|Delete Web Apps Instances Processes.|
|/sites/instances/processes/read|Get Web Apps Instances Processes.|
|/sites/instances/read|Get Web Apps Instances.|
|/sites/listsyncfunctiontriggerstatus/action|List Sync Function Trigger Status Web Apps.|
|/sites/metricdefinitions/read|Get Web Apps Metric Definitions.|
|/sites/metrics/read|Get Web Apps Metrics.|
|/sites/metricsdefinitions/read|Get Web Apps Metrics Definitions.|
|/sites/migratemysql/action|Migrate MySql Web Apps.|
|/sites/migratemysql/read|Get Web Apps Migrate MySql.|
|/sites/networktrace/action|Network Trace Web Apps.|
|/sites/newpassword/action|Newpassword Web Apps.|
|/sites/operationresults/read|Get Web Apps Operation Results.|
|/sites/operations/read|Get Web Apps Operations.|
|/sites/perfcounters/read|Get Web Apps Performance Counters.|
|/sites/premieraddons/delete|Delete Web Apps Premier Addons.|
|/sites/premieraddons/read|Get Web Apps Premier Addons.|
|/sites/premieraddons/write|Update Web Apps Premier Addons.|
|/sites/processes/read|Get Web Apps Processes.|
|/sites/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/sites/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/sites/providers/Microsoft.Insights/metricDefinitions/Read|Gets the available metrics for Web App|
|/sites/publiccertificates/delete|Delete Web Apps Public Certificates.|
|/sites/publiccertificates/read|Get Web Apps Public Certificates.|
|/sites/publiccertificates/write|Update Web Apps Public Certificates.|
|/sites/publish/Action|Publish a Web App|
|/sites/publishxml/Action|Get publishing profile xml for a Web App|
|/sites/publishxml/read|Get Web Apps Publishing XML.|
|/sites/Read|Get the properties of a Web App|
|/sites/recommendationhistory/read|Get Web Apps Recommendation History.|
|/sites/recommendations/disable/action|Disable Web Apps Recommendations.|
|/sites/recommendations/Read|Get the list of recommendations for web app.|
|/sites/recover/action|Recover Web Apps.|
|/sites/resetSlotConfig/Action|Reset web app configuration|
|/sites/resourcehealthmetadata/read|Get Web Apps Resource Health Metadata.|
|/sites/restart/Action|Restart a Web App|
|/sites/restore/read|Get Web Apps Restore.|
|/sites/restore/write|Restore Web Apps.|
|/sites/siteextensions/delete|Delete Web Apps Site Extensions.|
|/sites/siteextensions/read|Get Web Apps Site Extensions.|
|/sites/siteextensions/write|Update Web Apps Site Extensions.|
|/sites/slots/analyzecustomhostname/read|Get Web Apps Slots Analyze Custom Hostname.|
|/sites/slots/applySlotConfig/Action|Apply web app slot configuration from target slot to the current slot.|
|/sites/slots/backup/Action|Create new Web App Slot backup.|
|/sites/slots/backup/read|Get Web Apps Slots Backup.|
|/sites/slots/backup/write|Update Web Apps Slots Backup.|
|/sites/slots/backups/delete|Delete Web Apps Slots Backups.|
|/sites/slots/backups/list/action|List Web Apps Slots Backups.|
|/sites/slots/backups/Read|Get the properties of a web app slots' backup|
|/sites/slots/backups/restore/action|Restore Web Apps Slots Backups.|
|/sites/slots/config/delete|Delete Web Apps Slots Config.|
|/sites/slots/config/list/Action|List Web App Slot's security sensitive settings, such as publishing credentials, app settings and connection strings|
|/sites/slots/config/Read|Get Web App Slot's configuration settings|
|/sites/slots/config/Write|Update Web App Slot's configuration settings|
|/sites/slots/continuouswebjobs/delete|Delete Web Apps Slots Continuous Web Jobs.|
|/sites/slots/continuouswebjobs/read|Get Web Apps Slots Continuous Web Jobs.|
|/sites/slots/continuouswebjobs/start/action|Start Web Apps Slots Continuous Web Jobs.|
|/sites/slots/continuouswebjobs/stop/action|Stop Web Apps Slots Continuous Web Jobs.|
|/sites/slots/Delete|Delete an existing Web App Slot|
|/sites/slots/deployments/delete|Delete Web Apps Slots Deployments.|
|/sites/slots/deployments/log/read|Get Web Apps Slots Deployments Log.|
|/sites/slots/deployments/read|Get Web Apps Slots Deployments.|
|/sites/slots/deployments/write|Update Web Apps Slots Deployments.|
|/sites/slots/diagnostics/analyses/execute/Action|Run Web Apps Slots Diagnostics Analysis.|
|/sites/slots/diagnostics/analyses/read|Get Web Apps Slots Diagnostics Analysis.|
|/sites/slots/diagnostics/aspnetcore/read|Get Web Apps Slots Diagnostics for ASP.NET Core app.|
|/sites/slots/diagnostics/autoheal/read|Get Web Apps Slots Diagnostics Autoheal.|
|/sites/slots/diagnostics/deployment/read|Get Web Apps Slots Diagnostics Deployment.|
|/sites/slots/diagnostics/deployments/read|Get Web Apps Slots Diagnostics Deployments.|
|/sites/slots/diagnostics/detectors/execute/Action|Run Web Apps Slots Diagnostics Detector.|
|/sites/slots/diagnostics/detectors/read|Get Web Apps Slots Diagnostics Detector.|
|/sites/slots/diagnostics/frebanalysis/read|Get Web Apps Slots Diagnostics FREB Analysis.|
|/sites/slots/diagnostics/loganalyzer/read|Get Web Apps Slots Diagnostics Log Analyzer.|
|/sites/slots/diagnostics/read|Get Web Apps Slots Diagnostics.|
|/sites/slots/diagnostics/runtimeavailability/read|Get Web Apps Slots Diagnostics Runtime Availability.|
|/sites/slots/diagnostics/servicehealth/read|Get Web Apps Slots Diagnostics Service Health.|
|/sites/slots/diagnostics/sitecpuanalysis/read|Get Web Apps Slots Diagnostics Site CPU Analysis.|
|/sites/slots/diagnostics/sitecrashes/read|Get Web Apps Slots Diagnostics Site Crashes.|
|/sites/slots/diagnostics/sitelatency/read|Get Web Apps Slots Diagnostics Site Latency.|
|/sites/slots/diagnostics/sitememoryanalysis/read|Get Web Apps Slots Diagnostics Site Memory Analysis.|
|/sites/slots/diagnostics/siterestartsettingupdate/read|Get Web Apps Slots Diagnostics Site Restart Setting Update.|
|/sites/slots/diagnostics/siterestartuserinitiated/read|Get Web Apps Slots Diagnostics Site Restart User Initiated.|
|/sites/slots/diagnostics/siteswap/read|Get Web Apps Slots Diagnostics Site Swap.|
|/sites/slots/diagnostics/threadcount/read|Get Web Apps Slots Diagnostics Thread Count.|
|/sites/slots/diagnostics/workeravailability/read|Get Web Apps Slots Diagnostics Workeravailability.|
|/sites/slots/diagnostics/workerprocessrecycle/read|Get Web Apps Slots Diagnostics Worker Process Recycle.|
|/sites/slots/domainownershipidentifiers/read|Get Web Apps Slots Domain Ownership Identifiers.|
|/sites/slots/hostnamebindings/delete|Delete Web Apps Slots Hostname Bindings.|
|/sites/slots/hostnamebindings/read|Get Web Apps Slots Hostname Bindings.|
|/sites/slots/hostnamebindings/write|Update Web Apps Slots Hostname Bindings.|
|/sites/slots/hybridconnection/delete|Delete Web Apps Slots Hybrid Connection.|
|/sites/slots/hybridconnection/read|Get Web Apps Slots Hybrid Connection.|
|/sites/slots/hybridconnection/write|Update Web Apps Slots Hybrid Connection.|
|/sites/slots/hybridconnectionnamespaces/relays/delete|Delete Web Apps Slots Hybrid Connection Namespaces Relays.|
|/sites/slots/hybridconnectionnamespaces/relays/write|Update Web Apps Slots Hybrid Connection Namespaces Relays.|
|/sites/slots/hybridconnectionrelays/read|Get Web Apps Slots Hybrid Connection Relays.|
|/sites/slots/instances/deployments/read|Get Web Apps Slots Instances Deployments.|
|/sites/slots/instances/processes/delete|Delete Web Apps Slots Instances Processes.|
|/sites/slots/instances/processes/read|Get Web Apps Slots Instances Processes.|
|/sites/slots/instances/read|Get Web Apps Slots Instances.|
|/sites/slots/metricdefinitions/read|Get Web Apps Slots Metric Definitions.|
|/sites/slots/metrics/read|Get Web Apps Slots Metrics.|
|/sites/slots/migratemysql/read|Get Web Apps Slots Migrate MySql.|
|/sites/slots/networktrace/action|Network Trace Web Apps Slots.|
|/sites/slots/newpassword/action|Newpassword Web Apps Slots.|
|/sites/slots/operationresults/read|Get Web Apps Slots Operation Results.|
|/sites/slots/operations/read|Get Web Apps Slots Operations.|
|/sites/slots/perfcounters/read|Get Web Apps Slots Performance Counters.|
|/sites/slots/phplogging/read|Get Web Apps Slots Phplogging.|
|/sites/slots/premieraddons/delete|Delete Web Apps Slots Premier Addons.|
|/sites/slots/premieraddons/read|Get Web Apps Slots Premier Addons.|
|/sites/slots/premieraddons/write|Update Web Apps Slots Premier Addons.|
|/sites/slots/providers/Microsoft.Insights/diagnosticSettings/read|Gets the diagnostic setting for the resource|
|/sites/slots/providers/Microsoft.Insights/diagnosticSettings/write|Creates or updates the diagnostic setting for the resource|
|/sites/slots/providers/Microsoft.Insights/metricDefinitions/Read|Gets the available metrics for Web App Slot|
|/sites/slots/publiccertificates/read|Get Web Apps Slots Public Certificates.|
|/sites/slots/publiccertificates/write|Create or Update Web Apps Slots Public Certificates.|
|/sites/slots/publish/Action|Publish a Web App Slot|
|/sites/slots/publishxml/Action|Get publishing profile xml for Web App Slot|
|/sites/slots/Read|Get the properties of a Web App deployment slot|
|/sites/slots/resetSlotConfig/Action|Reset web app slot configuration|
|/sites/slots/resourcehealthmetadata/read|Get Web Apps Slots Resource Health Metadata.|
|/sites/slots/restart/Action|Restart a Web App Slot|
|/sites/slots/restore/read|Get Web Apps Slots Restore.|
|/sites/slots/restore/write|Restore Web Apps Slots.|
|/sites/slots/siteextensions/delete|Delete Web Apps Slots Site Extensions.|
|/sites/slots/siteextensions/read|Get Web Apps Slots Site Extensions.|
|/sites/slots/siteextensions/write|Update Web Apps Slots Site Extensions.|
|/sites/slots/slotsdiffs/Action|Get differences in configuration between web app and slots|
|/sites/slots/slotsswap/Action|Swap Web App deployment slots|
|/sites/slots/snapshots/read|Get Web Apps Slots Snapshots.|
|/sites/slots/sourcecontrols/Delete|Delete Web App Slot's source control configuration settings|
|/sites/slots/sourcecontrols/Read|Get Web App Slot's source control configuration settings|
|/sites/slots/sourcecontrols/Write|Update Web App Slot's source control configuration settings|
|/sites/slots/start/Action|Start a Web App Slot|
|/sites/slots/stop/Action|Stop a Web App Slot|
|/sites/slots/sync/action|Sync Web Apps Slots.|
|/sites/slots/triggeredwebjobs/delete|Delete Web Apps Slots Triggered WebJobs.|
|/sites/slots/triggeredwebjobs/read|Get Web Apps Slots Triggered WebJobs.|
|/sites/slots/triggeredwebjobs/run/action|Run Web Apps Slots Triggered WebJobs.|
|/sites/slots/usages/read|Get Web Apps Slots Usages.|
|/sites/slots/virtualnetworkconnections/delete|Delete Web Apps Slots Virtual Network Connections.|
|/sites/slots/virtualnetworkconnections/gateways/write|Update Web Apps Slots Virtual Network Connections Gateways.|
|/sites/slots/virtualnetworkconnections/read|Get Web Apps Slots Virtual Network Connections.|
|/sites/slots/virtualnetworkconnections/write|Update Web Apps Slots Virtual Network Connections.|
|/sites/slots/webjobs/read|Get Web Apps Slots WebJobs.|
|/sites/slots/Write|Create a new Web App Slot or update an existing one|
|/sites/slotsdiffs/Action|Get differences in configuration between web app and slots|
|/sites/slotsswap/Action|Swap Web App deployment slots|
|/sites/snapshots/read|Get Web Apps Snapshots.|
|/sites/sourcecontrols/Delete|Delete Web App's source control configuration settings|
|/sites/sourcecontrols/Read|Get Web App's source control configuration settings|
|/sites/sourcecontrols/Write|Update Web App's source control configuration settings|
|/sites/start/Action|Start a Web App|
|/sites/stop/Action|Stop a Web App|
|/sites/sync/action|Sync Web Apps.|
|/sites/syncfunctiontriggers/action|Sync Function Triggers for Web Apps.|
|/sites/triggeredwebjobs/delete|Delete Web Apps Triggered WebJobs.|
|/sites/triggeredwebjobs/history/read|Get Web Apps Triggered WebJobs History.|
|/sites/triggeredwebjobs/read|Get Web Apps Triggered WebJobs.|
|/sites/triggeredwebjobs/run/action|Run Web Apps Triggered WebJobs.|
|/sites/usages/read|Get Web Apps Usages.|
|/sites/virtualnetworkconnections/delete|Delete Web Apps Virtual Network Connections.|
|/sites/virtualnetworkconnections/gateways/read|Get Web Apps Virtual Network Connections Gateways.|
|/sites/virtualnetworkconnections/gateways/write|Update Web Apps Virtual Network Connections Gateways.|
|/sites/virtualnetworkconnections/read|Get Web Apps Virtual Network Connections.|
|/sites/virtualnetworkconnections/write|Update Web Apps Virtual Network Connections.|
|/sites/webjobs/read|Get Web Apps WebJobs.|
|/sites/Write|Create a new Web App or update an existing one|
|/skus/read|Get SKUs.|
|/sourcecontrols/read|Get Source Controls.|
|/sourcecontrols/write|Update Source Controls.|
|/unregister/action|Unregister Microsoft.Web resource provider for the subscription.|
|/validate/action|Validate .|
|/verifyhostingenvironmentvnet/action|Verify Hosting Environment Vnet.|

## <a name="microsoftworkloadmonitor"></a>Microsoft.WorkloadMonitor

| Operation | Description |
|---|---|
|/components/read|Read operations resources|
|/healthInstances/read|Read operations resources|
|/Operations/read|Read operations resources|
|/workloads/delete|Deletes a workload resource|
|/workloads/read|Reads a workload resource|
|/workloads/write|Writes a workload resource|

## <a name="next-steps"></a>Next steps

- Learn how to <bpt id="p1">[</bpt>create a custom role<ept id="p1">](role-based-access-control-custom-roles.md)</ept>.
- Review the <bpt id="p1">[</bpt>built in RBAC roles<ept id="p1">](role-based-access-built-in-roles.md)</ept>.
- Learn how to manage access assignments <bpt id="p1">[</bpt>by user<ept id="p1">](role-based-access-control-manage-assignments.md)</ept> or <bpt id="p2">[</bpt>by resource<ept id="p2">](role-based-access-control-configure.md)</ept> 
- Learn how to <bpt id="p1">[</bpt>View activity logs to audit actions on resources<ept id="p1">](~/articles/azure-resource-manager/resource-group-audit.md)</ept>
