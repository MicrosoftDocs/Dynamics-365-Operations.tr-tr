---
title: Banka günlüğü birleşik varlığını güncelleştirme
description: Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565938"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="b5afe-103">Banka günlüğü birleşik varlığını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b5afe-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5afe-104">Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b5afe-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="b5afe-105">Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="b5afe-106">Aşağıdaki banka günlüğü birleşik varlıklarını, varlıkları ve aşamalandırma tablolarını derleyin ve eşitleyin:</span><span class="sxs-lookup"><span data-stu-id="b5afe-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="b5afe-107">Birleşik Varlık\\BankaGünlükVarlığı</span><span class="sxs-lookup"><span data-stu-id="b5afe-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="b5afe-108">Varlık\\BankaGünlüğüBaşlıkVarlığı</span><span class="sxs-lookup"><span data-stu-id="b5afe-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="b5afe-109">Varlık\\BankaGünlüğüSatırVarlığı</span><span class="sxs-lookup"><span data-stu-id="b5afe-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="b5afe-110">Tablo\\BankaGünlüğüBaşlıkHazırlığı</span><span class="sxs-lookup"><span data-stu-id="b5afe-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="b5afe-111">Tablo\\BankaGünlüğüSatırHazırlığı</span><span class="sxs-lookup"><span data-stu-id="b5afe-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="b5afe-112">Veri yönetimi\\veri projeleri</span><span class="sxs-lookup"><span data-stu-id="b5afe-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="b5afe-113">**Kaynak Veri** yerleşiminde **Banka Hareketi** türünü gösterin.</span><span class="sxs-lookup"><span data-stu-id="b5afe-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="b5afe-114">Kaynak veri biçimi = XML Öğesi</span><span class="sxs-lookup"><span data-stu-id="b5afe-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="b5afe-115">Varlık adı = Banka Günlüğü</span><span class="sxs-lookup"><span data-stu-id="b5afe-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="b5afe-116">Yükleme veri dosyası = yeni sürüm ÖrnekBankaGünlüğüBirleşikVarlığı.xml</span><span class="sxs-lookup"><span data-stu-id="b5afe-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="b5afe-117">Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="b5afe-118">Eşlemeyi sıfırdan oluşturmak için **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="b5afe-119">Banka Hareketi Türü'nün eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="b5afe-120">Satır varlığında **Haritayı görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="b5afe-121">Banka Hareket Türü'nün Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="b5afe-122">Yeni ekstreyi içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="b5afe-122">Import the new statement.</span></span>




