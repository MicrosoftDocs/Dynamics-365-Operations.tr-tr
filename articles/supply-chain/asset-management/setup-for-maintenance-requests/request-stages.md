---
title: Bakım talebi yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde bakım talebi yaşam döngüsü durumları ayarlama işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b54b58a29dc23e19f5065363c331351f24267ac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360958"
---
# <a name="maintenance-request-lifecycle-states"></a>Bakım talebi yaşam döngüsü durumları

[!include [banner](../../includes/banner.md)]

 


Bakım talebi yaşam döngüsü durumları bir isteğin gidebileceği aşamaları tanımlar. Örneğin, **Oluşturulan**, **Etkin** ve **Sona ermiş** örnekler de içerir. Bir bakım isteği iş emrine dönüştürüldüğünde, bakım talebinin artık etkin olmadığını göstermek üzere sürdürme isteği yaşam döngüsü durumu **sonlandırıldı** veya **Kapalı** olarak güncelleştirilmelidir. **Tüm bakım talepleri** listesi sayfasında, yaşam döngüsü durumlarından bağımsız olarak tüm bakım taleplerini görebilirsiniz.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Bakım talebi yaşam döngüsü durumlarını ayarla

1. **Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü durumları**'nı seçin.
2. Bakım talebi yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.
3. **Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.
4. **Ad** alanına, bir ad girin.

    **Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü modelleri** alanı bu yaşam döngüsü durumunu kullanan bakım talebi yaşam döngüsü modellerinin sayısını gösterir.

5. **Genel** hızlı sekmesinde, bakım talebinin bu yaşam döngüsü durumunda etkin olması gerekiyorsa, **etkin** seçeneğini **Evet** olarak ayarlayın.
6. Gerçek bitiş tarihi ve saatinin bu yaşam döngüsü durumunda olan bir bakım isteğine otomatik olarak girilmesi gerekiyorsa, **Fiili bitiş ayarla** seçeneğini **Evet** olarak ayarlayın.
7. İş emri , bu yaşam döngüsü durumunda olan bir bakım talebinden oluşturulduysa, **İş emrini oluştur** seçeneğini **Evet** olarak ayarlayın.
8. Bir bakım talebi bu yaşam döngüsü durumundayken silinebilecekse, **Sil** seçeneğini **Evet** olarak ayarlayın.
9. **Güncelleştirme** hızlı sekmesinde, **Varlık** bölümündeki **Gelen** ve **Giden** seçenekleri depo onarımı görürseniz geçerlidir. Bakım isteğinde seçilen varlıkların varlık yaşam döngüsü durumunun, bu bakım talebinin bakım talebi yaşam döngüsü durumu **Gelen** veya **Giden** olarak ayarladığında, otomatik olarak **Gelen** veya **Giden** olarak güncelleştirilmesi gerekiyorsa ilgili seçeneği **Evet** olarak ayarlayın.

Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü durumları** sayfasının bir örneği gösterilmektedir.

![Bakım talebi yaşam döngüsü durumları sayfası.](media/02-setup-for-requests.png)

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

    - Yaşam döngüsü modeline bir yaşam döngüsü durumu eklemek istiyorsanız, modeli **Kalan yaşam döngüsü durumları** bölümünde seçin ve sonra sağ ok düğmesini ![Sağ ok.](media/03-setup-for-requests.png) seçerek **Seçilen yaşam döngüsü durumları** bölümüne taşıyın.
    - Yaşam döngüsü modelinde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir durumları seç** düğmesini ![Tüm kullanılabilir durumları seç.](media/04-setup-for-requests.png) seçin. Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.
    - Yaşam döngüsü modelinden bir yaşam döngüsü durumunu kaldırmak istiyorsanız, modeli **Seçili yaşam döngüsü durumları** bölümünde seçin ve sonra sol ok düğmesini ![Sol ok.](media/05-setup-for-requests.png) seçerek **Kalan döngüsü durumları** bölümüne taşıyın.

6. **Genel** hızlı sekmesinde, depot onarımını kullanırsanız, **Güncelleştirmeler** bölümündeki alanlar geçerlidir.

    - **Alınan varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların depot onarımı için alındıkları sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.
    - **Verilen varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların onarımdan sonra döndükleri sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.

Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü modelleri** sayfasının bir örneği gösterilmektedir.

![Bakım talebi yaşam döngüsü modelleri sayfası.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]