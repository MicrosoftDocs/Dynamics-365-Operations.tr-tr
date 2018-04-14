---
title: "Çağrı merkezi kataloğu oluşturma"
description: "Bu makalede bir çağrı merkezine yönelik bir katalog oluşturulması sürecine genel bir bakış sunulmuştur."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29d005655856fd1eb0f1490c45e07649465539f2
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-call-center-catalog"></a>Çağrı merkezi kataloğu oluşturma

[!INCLUDE [banner](includes/banner.md)]

Bu makalede bir çağrı merkezine yönelik bir katalog oluşturulması sürecine genel bir bakış sunulmuştur. 

Bir çağrı merkezinde ürün kataloglarını müşterilere sunmak istediğiniz ürünleri belirlemek için kullanabilirsiniz. Çağrı merkezleri genellikle basılı kataloglar kullanır. Basılı bir kataloğun tasarımı ve üretimi Microsoft Dynamics 365 for Retail dışında yapılır. Ancak, çevrimiçi perakende kataloglarını ayarlamak için kullandığınız aynı biçimleri kullanarak bir kataloğun dijital biçimini oluşturabilir ve saklayabilirsiniz. Bir katalog oluşturmak için önce ürün sınıflamalar ayarlayıp sınıflamaları bir çağrı merkezine atayın. Sonra ürün kataloğuna ürünleri bu sınıflamalardan seçerek ekleyin. Ürün kataloğuna eklendikten ve Katalog tamamlandıktan sonra verileri doğrulamak için katalogu doğrulamalısınız. Ardından kataloğu gözden geçirme ve onay için gönderin. Katalog onaylandıktan sonra yayımlanabilir. Bir çağrı merkezi katalogu oluşturulduğunda, katalog yayınlandığı zaman katalog verilerinin bir ekran görüntüsünü alabilirsiniz. Bu anlık görüntü işlevselliği belirli bir sürüm için katalog daha sonra değiştirilmiş ve güncelleştirilmiş olsa bile kataloga erişmenizi sağlar. Çağrı merkezi kataloglarını aşağıdaki isteğe bağlı özellikleri içerecek şekilde de ayarlayabilirsiniz.

-   **Kaynak kodları** – Belirli katalog postalarına müşterinin tepkisini izlemek için kullanılan kodlar.
-   **Ücretsiz ürünler** – Bir müşterinin siparişine ek ücret olmaksızın dahil edilen ürünler. Siparişe kataloğun kaynak kodu girildiğinde, bu ürünler de otomatik olarak siparişe eklenir.
-   **Senaryolar** – satış siparişi oluşturulduğunda, çağrı merkezi çalışanının bir müşteriye okuyacağı metinler. Komut dosyaları tebrik veya satın alma önerileri içerebilir.
-   **Dikey satış veya yukarı satış ürünleri** - Belirli bir ürün siparişe eklendiğinde bir öneri olarak görüntülenen ürünler.

Bu seçeneklerin katalog onaylanmadan ve yayınlanmadan önce ayarlanması gerekir.

## <a name="prerequisites"></a>Önkoşullar
Başlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir:

-   Ürünleri ve ürün çeşitlerini ayarlayın.
-   Perakende ürünleri ayarlayın.
-   Bir ürün çeşidi ayarlayın.
-   Bir çağrı merkezi oluşturun.
-   Bir çağrı merkezi ayarlayın.
-   Çağrı merkezini bir organizasyon hiyerarşisine ekleyin.
-   Bir organizasyon hiyerarşisi oluşturun veya değiştirin.

## <a name="create-a-catalog"></a>Katalog oluşturma
İlk önce bir katalog oluşturmanız, kataloğa ürün eklemeniz ve sonraysa ürünlerin özniteliklerini gözden geçirmeniz ve güncellemeniz gerekir.

## <a name="validate-the-catalog"></a>Kataloğu doğrulama
Katalog ayarlarını yaptıktan sonra kataloğu doğrulamanız gerekir. Doğrulama işlemi, kanal öznitelikleri ve ürün öznitelikleri için gerekli olan verilerin tam ve geçerli olduğunu ve kataloğun yayınlanabilir olduğunu doğrular.

## <a name="submit-the-catalog-for-review-and-approval"></a>Kataloğu onay için gözden geçirme ve gönderme
Bir katalog doğrulandıktan sonra gözden geçirme ve onay için gönderebilirsiniz. Katalog yayınlanmadan önce onaylanmalıdır. İş akışını kataloglar otomatik olarak onaylanacak ya da el ile onay gerektirecek şekilde yapılandırabilirsiniz.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>İsteğe bağlı: Kaynak kodlar, ücretsiz ürünler ve senaryolar ekleme
Bir çağrı merkezi kataloğuna aşağıdaki öğeleri de ekleyebilirsiniz. Bunlar isteğe bağlıdır.

-   **Kaynak kodları** Müşterinin özel kataloglara verdiği tepkiyi izlemek için basılı kataloglar sağlayan şirketler tarafından kullanılabilir. Kaynak kodları genellikle bir kataloğun arkasında yazılıdır ve satış siparişine, bir müşteri satın alma yaptığında girilir. Kataloğa bir kaynak kodu eklemek için önce bir hedef pazar oluşturmanız gerekir. Hedef pazar genellikle sahip olunan veya kiralanmış bir postalama listesiyle eşleştirilir.
-   **Ücretsiz ürünler** kataloğa başvurulduğunda müşterinin siparişine ücretsiz eklenen promosyon ürünleridir.
-   **Senaryolar** bir kataloğun içeriğinde veya katalogdaki bir üründe çalışanın müşterilerle etkileşimlerinde yol gösterici olarak kullanılabilir.

## <a name="publish-the-catalog"></a>Kataloğu yayınlama
Bir katalog yayımlayarak, katalogdaki ürün bilgilerine son şeklini vermiş olursunuz. Yayınlama, kataloğun gerçekleştirmek istediğiniz diğer işlemler için de hazır olduğunu gösterir. Örneğin, basılı bir katalog oluşturabilirsiniz. Kataloglarınızı el ile yayınlayabilir veya bir plana göre yayınlamak için bir toplu işlem kullanabilirsiniz. Bir kataloğu yayınlayabilmeniz için doğrulanmış ve onaylanmış olması gerekir. Kataloğu yayınlandıktan sonra değiştirmek için kataloğu geri alabilir ve sonra yeniden yayınlayabilirsiniz.




