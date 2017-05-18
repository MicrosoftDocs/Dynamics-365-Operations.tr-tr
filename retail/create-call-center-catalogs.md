---
title: "Çağrı merkezi kataloğu oluşturma"
description: "Bu makalede bir çağrı merkezine yönelik bir katalog oluşturulması sürecine genel bir bakış sunulmuştur."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 30a782611a47e662de4f8c30c29e613b44dcc953
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="create-a-call-center-catalog"></a>Çağrı merkezi kataloğu oluşturma

[!include[banner](includes/banner.md)]


Bu makalede bir çağrı merkezine yönelik bir katalog oluşturulması sürecine genel bir bakış sunulmuştur. 

Bir çağrı merkezinde ürün kataloglarını müşterilere sunmak istediğiniz ürünleri belirlemek için kullanabilirsiniz. Çağrı merkezleri genellikle basılı kataloglar kullanır. Basılı bir kataloğun tasarımı ve üretimi Microsoft Dynamics 365 for Operations dışında yapılır. Ancak, çevrimiçi perakende kataloglarını ayarlamak için kullandığınız aynı formları kullanarak bir kataloğun dijital biçimini Dynamics 365 for Operations'ta Perakende ve ticaret alanında oluşturabilir ve saklayabilirsiniz. Bir katalog oluşturmak için önce ürün sınıflamalar ayarlayıp sınıflamaları bir çağrı merkezine atayın. Sonra ürün kataloğuna ürünleri bu sınıflamalardan seçerek ekleyin. Ürün kataloğuna eklendikten ve Katalog tamamlandıktan sonra verileri doğrulamak için katalogu doğrulamalısınız. Ardından kataloğu gözden geçirme ve onay için gönderin. Katalog onaylandıktan sonra yayımlanabilir. Bir çağrı merkezi katalogu oluşturulduğunda, katalog yayınlandığı zaman katalog verilerinin bir ekran görüntüsünü alabilirsiniz. Bu anlık görüntü işlevselliği belirli bir sürüm için katalog daha sonra değiştirilmiş ve güncelleştirilmiş olsa bile kataloga erişmenizi sağlar. Çağrı merkezi kataloglarını aşağıdaki isteğe bağlı özellikleri içerecek şekilde de ayarlayabilirsiniz.

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




