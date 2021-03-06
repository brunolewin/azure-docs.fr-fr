---
title: Présentation du Stockage Blob - Stockage d’objets dans Azure | Microsoft Docs
description: Le Stockage Blob Azure est conçu pour stocker de grandes quantités de données d’objet non structurées, telles que des données texte ou binaires. Vos applications peuvent accéder aux objets du stockage Blob à partir de PowerShell ou d’Azure CLI, à partir du code via des bibliothèques clientes de stockage Azure ou par REST.
services: storage
author: tamram
manager: jeconnoc
ms.service: storage
ms.topic: overview
ms.date: 03/27/2018
ms.author: tamram
ms.openlocfilehash: 0fff0032ec2452413bcd1df3175634b14a64208f
ms.sourcegitcommit: c3d53d8901622f93efcd13a31863161019325216
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2018
---
# <a name="introduction-to-blob-storage"></a>Présentation du Stockage Blob

Le Stockage Blob Azure est la solution de stockage cloud de Microsoft pour les objets de données. Le Stockage Blob peut stocker de grandes quantités de données d’objet non structurées, telles que des données texte ou binaires. Les données du Stockage Blob sont accessibles n’importe où dans le monde via HTTP ou HTTPS. Vous pouvez utiliser le stockage d'objets blob pour exposer les données publiquement dans le monde ou pour le stockage privé de données d'applications.

Voici quelques utilisations courantes du stockage d’objets blob :

* Mise à disposition d’images ou de documents directement dans un navigateur
* Stockage de fichiers pour un accès distribué
* Diffusion en continu de vidéo et d’audio
* Stockage pour la sauvegarde et la restauration, la récupération d’urgence et l’archivage
* Stockage des données pour l’analyse par un service local ou hébergé par Azure
* Stockage des VHD pour l’utilisation avec des machines virtuelles Azure

## <a name="blob-service-concepts"></a>Concepts du service BLOB

Le service d’objets blob contient les composants suivants :

![Architecture d’objets blob](./media/storage-blobs-introduction/blob1.png)

* **Compte de stockage :** tout accès au stockage Azure s'effectue via un compte de stockage. Ce compte de stockage peut être un **Compte de stockage à usage général (v1 ou v2)** ou **Compte de stockage blob**. Pour plus d’informations, voir [À propos des comptes de stockage Azure](../common/storage-create-storage-account.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json).

* **Conteneur :** un conteneur regroupe un ensemble d'objets blob. Tous les objets blob doivent figurer dans un conteneur. Un compte peut contenir un nombre illimité de conteneurs. Un conteneur peut stocker un nombre illimité d’objets blob. Notez que le nom du conteneur doit être en minuscules.

* **Objet blob :** fichier de tout type et de toute taille. Stockage Azure propose trois types d’objets blob : les objets blob de blocs, les [objets blob de pages](storage-blob-pageblob-overview.md) et les objets blob d’ajouts.
  
    Les *objets blob de blocs* sont parfaits pour le stockage des fichiers texte ou binaires, tels que les documents et les fichiers multimédias. Les *objets blob d’ajout* sont similaires aux objets blob de blocs dans la mesure où ils sont composés de blocs. Cependant, ils sont optimisés pour les opérations d’ajouts et sont donc utiles pour les scénarios de journalisation. Un objet blob de blocs ou d’ajouts peut contenir jusqu’à 50 000 blocs de 100 Mo chacun, soit une taille totale légèrement supérieure à 4,75 Go (100 Mo x 50 000). Un objet blob d’ajout peut contenir jusqu’à 50 000 blocs de 4 Mo chacun, soit une taille totale légèrement supérieure à 195 Go (4 Mo x 50 000).
  
    La taille maximale des *objets blob de pages* peut atteindre 8 To. Ces objets sont plus efficaces pour les opérations fréquentes de lecture/écriture. Azure Virtual Machines utilise des objets blob de pages comme disques de données et disques du système d’exploitation.
  
    Pour plus de détails sur l’affectation de noms aux conteneurs et objets blob, consultez [Affectation de noms et références aux conteneurs, objets blob et métadonnées](/rest/api/storageservices/Naming-and-Referencing-Containers--Blobs--and-Metadata).

## <a name="next-steps"></a>Étapes suivantes

* [Créez un compte de stockage](../common/storage-create-storage-account.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)
* [Prise en main du Stockage Blob avec .NET](storage-dotnet-how-to-use-blobs.md)
* [Exemples relatifs au service Stockage Azure avec .NET](../common/storage-samples-dotnet.md)
* [Exemples relatifs au service Stockage Azure avec Java](../common/storage-samples-java.md)
