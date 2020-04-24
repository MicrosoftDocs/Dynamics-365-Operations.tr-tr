---
title: Bakım talebi yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde bakım talebi yaşam döngüsü durumları ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1e4412af0619b57467b5bcba75ea7259604d1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209019"
---
# <a name="maintenance-request-lifecycle-states"></a>Bakım talebi yaşam döngüsü durumları

[!include [banner](../../includes/banner.md)]

 


Bakım talebi yaşam döngüsü durumları bir isteğin gidebileceği aşamaları tanımlar. Örneğin, **Oluşturulan**, **Etkin**ve **Sona ermiş** örnekler de içerir. Bir bakım isteği iş emrine dönüştürüldüğünde, bakım talebinin artık etkin olmadığını göstermek üzere sürdürme isteği yaşam döngüsü durumu **sonlandırıldı** veya **Kapalı** olarak güncelleştirilmelidir. **Tüm bakım talepleri** listesi sayfasında, yaşam döngüsü durumlarından bağımsız olarak tüm bakım taleplerini görebilirsiniz.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Bakım talebi yaşam döngüsü durumlarını ayarla

1. **Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü durumları**'nı seçin.
2. Bakım talebi yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.
3. **Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.
4. **Ad** alanına, bir ad girin.

    **Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü modelleri** alanı bu yaşam döngüsü durumunu kullanan bakım talebi yaşam döngüsü modellerinin sayısını gösterir.

5. **Genel** hızlı sekmesinde, bakım talebinin bu yaşam döngüsü durumunda etkin olması gerekiyorsa, **etkin** seçeneğini **Evet** olarak ayarlayın.
6. Gerçek bitiş tarihi ve saatinin bu yaşam döngüsü durumunda olan bir bakım isteğine otomatik olarak girilmesi gerekiyorsa, **fiili bitiş** seçeneğini **Evet** olarak ayarlayın.
7. İş emri , bu yaşam döngüsü durumunda olan bir bakım talebinden oluşturulduysa, **İş emrini oluştur** seçeneğini **Evet** olarak ayarlayın.
8. Bir bakım talebi bu yaşam döngüsü durumundayken silinebilecekse, **Sil** seçeneğini **Evet** olarak ayarlayın.
9. **Güncelleştir** hızlı sekmesinde, depo onarımını kullanırsanız ,**Varlık** bölümündeki **gelen** ve **giden** seçenekleri geçerlidir. Bakım talebinde seçilen varlıkların yaşam döngüsü durumu otomatik olarak **Gelen** ya da **Giden** olarak güncelleştirilecekse ilgili seçeneği **Evet** olarak ayarlayın; söz konusu bakım talebinin bakım talebi yaşam döngüsü durumu **Gelen** ya da **Giden** olarak ayarlandığında.

Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü durumları** sayfasının bir örneği gösterilmektedir.

![Bakım talebi yaşam döngüsü durumları sayfası](media/02-setup-for-requests.png)

> [!NOTE]
> Bakım talebi yaşam döngüsü durumları, yaşam döngüsü durum grupları ve türlerin ilişkili olduğu ve iş emri yaşam döngüsü durumları, yaşam döngüsü durumu grupları ve türlerle aynı şekilde kullanıldığı gibi kullanılabilir. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Bakım talebi yaşam döngüsü modellerini ayarla

Bakım talepleriniz için gerekli yaşam döngüsü durumları oluşturulduktan sonra, yaşam döngüsü durum gruplarına veya yaşam döngüsü modellerine ayrılabilir. Bakım talebi yaşam döngüsü modelleri, farklı türlerde bakım istekleri için kullanılabilecek akışı oluşturmak için kullanılır. En az bir standart bakım talebi yaşam döngüsü modeli oluşturulmalıdır.

1. **Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü modelleri**'ni seçin.
2. Bakım talebi yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.
3. **Yaşam döngüsü modeli** alanında yaşam döngüsü modeli kimliğini girin.
4. **Ad** alanına, bir ad girin.

    **Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü durumları** alanı ilgili yaşam döngüsü modelinde seçili yaşam döngüsü durumlarının sayısını gösterir. **Bakım talebi türleri** alanı bu yaşam döngüsü modelini kullanan bakım talebi türlerinin sayısını gösterir.

5. **Yaşam döngüsü durumları** hızlı sekmesinde yaşam döngüsü modeline eklenmesi gereken yaşam döngüsü durumlarını seçin:

    - Yaşam döngüsü modelinde bir yaşam döngüsü durumu kullanmak için durumu **Kalan yaşam döngüsü durumları** bölümünden seçin ve sağ ok düğmesini ![Sağ ok](media/03-setup-for-requests.png) seçerek durumu **Seçili yaşam döngüsü durumları** bölümüne taşıyın.
    - Yaşam döngüsü modelinde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir durumları seç** düğmesini ![Tüm kullanılabilir durumları seç](media/04-setup-for-requests.png) seçin. Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.
    - Yaşam döngüsü modelinden bir yaşam döngüsü durumunu kaldırmak için durumu **Seçili yaşam döngüsü durumları** bölümünden seçin ve sol ok düğmesini ![Sol ok](media/05-setup-for-requests.png) seçerek durumu **Kalan yaşam döngüsü durumları** bölümüne taşıyın.

6. **Genel** hızlı sekmesinde, depot onarımını kullanırsanız, **Güncelleştirmeler** bölümündeki alanlar geçerlidir.

    - **Alınan varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların depot onarımı için alındıkları sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.
    - **Verilen varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların onarımdan sonra döndükleri sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.

Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü modelleri** sayfasının bir örneği gösterilmektedir.

![Bakım talebi yaşam döngüsü modelleri sayfası](media/06-setup-for-requests.png)
