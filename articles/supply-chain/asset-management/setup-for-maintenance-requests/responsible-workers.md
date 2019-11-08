---
title: Sorumlu bakım görevlileri
description: Bu konuda Varlık Yönetimi'nde sorumlu bakım görevlisi ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f436ffd01ac56bb4bc0021e226dad46d7c3377
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569927"
---
# <a name="responsible-maintenance-workers"></a>Sorumlu bakım görevlileri

[!include [banner](../../includes/banner.md)]

 

Sorumlu bakım görevlisi, varlık türleri, varlıklar, işlem yapılacak yerleşim, bakım işi türü kategorileri, bakım işi türleri, bakım işi türü türevleri ve ticaret ile ilgili olabilir. İş emri ve bakım taleplerinde, çalışma emrinden sorumlu olması gereken bakım görevlileri hakkında bir tercih belirtmek için kullanılabilir. (Ancak, bu bakım görevlileri mutlaka iş emrini yürütmek için planlanan aynı çalışanlar değildir.) Bu işlevin kullanılması isteğe bağlıdır. Örneğin, belirli iş türleri veya çalışma alanları için sorumlu çalışanlaro veya çalışan gruplarını seçmek için kullanılabilir.

İş emri yaşam döngüsü veya bakım talebi yaşam döngüsü sırasında, sorumlu bakım görevlileri değiştirilebilir veya güncelleştirilebilir. Bu değişiklik veya güncelleştirme, örneğin, bakım talebi yaşam döngüsü durumu veya iş emri yaşam döngüsü durumunda bir değişiklik ile ilgili olabilir.

**Sorumlu bakım görevlileri** sayfasındaki kurulum, iş emri planlaması sırasında *kullanılmaz*.

> [!NOTE]
> Varlık Yönetimi'nde, iş emri planlaması sırasında iş emirlerine tahsis edilebilecek *tercih edilen* bakım görevlisini de ayarlayabilirsiniz.

Sorumlu bakım görevlilerini ayarlaymadan önce, seçim için kullanılabilir olması gereken işçiler ve bakım görevlilerinin gruplarını ayarlamanız gerekir. (Çalışan ve bakım görevlileri gruplarını nasıl ayarlayacağınızla ilgili daha fazla bilgi için bkz: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).)

## <a name="set-up-responsible-maintenance-workers"></a>Sorumlu bakım görevlilerini ayarla

1. **Kıymet yönetimi** \> **Kurulum** \> **Çalışanlar** \> **Sorumlu bakım görevlileri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. Öncelikle yalnızca **Sorumlu bakım görevlisi** alanını ve/veya **Sorumlu çalışan** alanını ayarladığınız varsayılan sorumlu bakım görevlisi veya sorumlu bakım görevlisi grubu kurulumunu oluşturun. Kalan alanları boş bırakın. Bu varsayılan kurulum, iş emri planlaması sırasında başka, daha özel kombinasyon iş emrinin içeriğiyle eşleşirse kullanılacaktır.

    > [!NOTE]
    > Bir bakım talebinin yaratılması sırasında, **Tüm bakım talepleri** sayfasında seçim için sorumlu bir bakım görevlisi veya sorumlu bakım görevlisi grubu oluşturulduğunda, Varlık Yönetimi olası bir eşleşmeyi kontrol etmek için tüm sorumlu bakım görevlisi kayıtlarını kontrol eder. Her zaman ilk önce en belirgin birleşimi denetler. Diğer bir deyişle, Kıymet Yönetimi önce **Ticaret** alanı için bir eşleşme arar. Eşleşme bulamazsa **Bakım işi** alanı için eşleşmeleri denetler. Eşleşme bulamazsa **Bakım işi türü** alanı için eşleşmeleri denetler ve bu şekilde devam eder. Sayfanın mizanpajında gördüğünüz gibi bu davranış en spesifik kombinasyonu bulmak için varlık yönetimi, her kaydı sağdan sola doğru kontrol eder (ilk önce **Ticaret**, sonra **Bakım işi türü varyantı**, sonra **Bakım işi türü**, sonra **Bakım işi türü kategorisi**, sonra **İşlem yapılacak yerleşim**, sonra **Varlık** ve son olarak **Varlık türü**). Eşleşme bulunmazsa, bu yedi alanda hiçbir seçimi olmayan varsayılan kayıt kullanılır.

Aşağıdaki çizimde bir **Sorumlu bakım görevlileri** liste sayfasının bir örneği gösterilmektedir.

![Sorumlu bakım görevlileri sayfası](media/08-setup-for-requests.png)
