---
title: Not tümleştirmesi
description: Bu makalede, not verilerinin çift yazmada tümleştirilmesi açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f09d455181b7929e25d5238949a0236ac60d457b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289031"
---
# <a name="note-integration"></a>Not tümleştirmesi

[!include [banner](../../includes/banner.md)]



İş süreçleri sırasında, Microsoft Dynamics 365 kullanıcıları genellikle müşterileri hakkında bilgi toplar. Bu bilgiler aktiviteler ve notlar olarak kaydedilir. Bu makalede, not verilerinin çift yazmada tümleştirilmesi açıklanmaktadır.

Müşteri bilgileri aşağıdaki yollarla sınıflandırılabilir:

+ **Bir Dynamics 365 kullanıcısının bir müşteri adına işlediği eyleme dönüştürülebilen bilgiler**: Örneğin, Contoso (bir Dynamics 365 kullanıcısı) bir oyun gösterisi yürütüyor. Contoso müşterilerinden biri (bir müşteri) oyun gösterisine katılmak istiyor. Müşteri, bir contoso çalışanından kendisi için oyun gösterisinde bir yer ayırtmasını istiyor. Kayıt, Contoso'nun etkinlik katılımcı takvimine işleniyor.
+ **Bir Dynamics 365 kullanıcısı için eyleme dönüştürülebilen bilgiler**: Örneğin, bir Surface birimi satın alan bir müşteri, cihazın teslim edilmeden önce hediye paketi yapılmasını belirten özel talimatlar giriyor. Bu talimatlar paketlemeden sorumlu olan Contoso çalışanı tarafından işlenmesi gereken, eyleme dönüştürülebilen bilgilerdir.
+ **Eyleme dönüştürülemeyen bilgiler**: Örneğin, bir müşteri Contoso mağazasını ziyaret eder ve mağaza görevlisiyle konuşmaları sırasında *Halo* oyunları ve oyun aksesuarlarıyla ilgilendiğini ifade eder. Mağaza görevlisi bu bilgiyi not eder. Daha sonra, ürün öneri altyapısı bunu müşteriye önerilerde bulunmak için kullanır.

Genel olarak, eyleme dönüştürülebilen bilgiler, finans ve operasyon uygulamaları ve müşteri etkileşimi uygulamalarında *etkinlikler* olarak kaydedilir. Eyleme dönüştürülemeyen bilgiler, finans ve operasyon uygulamalarında *notlar* ve müşteri etkileşimi uygulamalarında *ek açıklamalar* olarak kaydedilir.

> [!TIP]
> Notlar, eyleme dönüştürülemeyen bilgiler için düşünülse de, uygulamalar bu notları bu şekilde kullanmak isterseniz bunları kaydedip eyleme dönüştürülebilir bilgi olarak kullanmanızı engellemez.

Microsoft, şu anda not tümleştirme işlevini yayımlamaktadır. (Faaliyet entegrasyonu işlevi daha sonra yayımlanacaktır.) Not Tümleştirme, müşteriler, satıcılar, satış siparişleri ve satın alma siparişleri için kullanılabilir.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Customer engagement uygulamasında bir not oluşturma

Bir müşteri etkileşimi uygulamasında bir not oluşturmak ve sonra bir finans ve operasyon uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Customer engagement uygulamasında bir müşteri için hesap kaydı açın.
2. **Zaman çizelgesi** bölmesinde artı işaretini (**+**) seçin ve sonra Not oluşturmak için **Not**'u seçin.

    ![Customer engagement uygulamasında bir not oluşturma.](media/notes-ce-1.png)

3. Bir başlık ve açıklama girin ve sonra **Not ekle**'yi seçin.

    ![Bir başlık ve açıklama girme.](media/notes-ce-2.png)

    Yeni Not Müşteri zaman çizelgesine eklenir.

    ![Müşteri zaman çizelgesindeki yeni Not.](media/notes-ce-3.png)

4. Finans ve operasyon uygulamasında oturum açın ve aynı müşteri kaydını açın. Sağ üst köşedeki **ekler** düğmesi (ataş simgesi) kaydın bir eki olduğunu belirtir.

    ![Ek hakkında bildirim.](media/notes-ce-4.png)

5. **Ekler** sayfasını açmak için **ekler** düğmesini seçin. Customer engagement uygulamasında oluşturduğunuz notu bulmanız gerekir.

    ![Customer Engagement uygulamasındaki not.](media/notes-ce-5.png)

Notta yapılan güncelleştirmeler, finans ve operasyon uygulaması ve müşteri etkileşimi uygulaması arasında eşitlenir.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Finans ve operasyon uygulamasında not oluşturma

Finans ve operasyon uygulamasında da bir not oluşturabilirsiniz ve bu not müşteri etkileşimi uygulamasıyla eşitlenir.

Bir finans ve operasyon uygulamasında not oluşturmak ve sonra bir müşteri etkileşimi uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finans ve operasyon uygulamasında, **Ekler** sayfasında **Yeni** \> **Not**'u seçin.

    ![Finans ve operasyon uygulamasında not oluşturulur.](media/notes-fo-1.png)

2. Bir başlık ve kısa bir yönerge kümesi girip **Kaydet**'i seçin.

    ![Bir başlık ve yönerge girme.](media/notes-fo-2.png)

3. Customer engagement uygulamasında kaydı güncelleştirin. Yeni notu zaman çizelgesinde bulmanız gerekir.

    ![Customer Engagement uygulamasında zaman çizelgesindeki yeni Not.](media/notes-fo-3.png)

Bir notu dahili veya harici olarak sınıflandırabilirsiniz.

- Finans ve operasyon uygulamasında, **Ekler** sayfasında notu açın ve sonra **Sınırlama** alanında **Dahili** veya **Harici** seçeneğini belirleyin.

    ![Sınırlama alanı.](media/notes-fo-4.png)

Ayrıca bir URL oluşturabilirsiniz.

1. Finans ve operasyon uygulamasında, **Ekler** sayfasında **Yeni** \> **URL**'yi seçin.
2. Bir başlık ve URL'yi girin.
3. **Sınırlama** alanında, **dahili** veya **harici** seçeneğini belirleyin.

    ![Finans ve operasyon uygulamasında URL oluşturulur.](media/notes-fo-5.png)

4. **Kaydet**'i seçin.

    Customer engagement uygulamalarının URL türleri olmadığından, URL not olarak çift yazmayla tümleştirilir.

    ![Customer Engagement uygulamasında not olarak görünen URL.](media/notes-ce-6.png)

> [!NOTE]
> Dosya ekleri desteklenmez.

## <a name="templates"></a>Şablonlar

Not tümleştirmesi aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir tablo eşlemeleri koleksiyonu içerir.

| Finans ve operasyon uygulaması | Müşteri etkileşimi uygulaması | Açıklama |
|----------------------------|-------------------------|-------------|
| [Müşteri ekleri](mapping-reference.md#230) | Ek açıklamalar | Müşteriye özel bilgileri (hem kuruluşlar, hem de kişiler için) yakalamak üzere düz metin ve URL kullanan işletmeler. |
| [Satıcı belgesi ekleri](mapping-reference.md#231) | Ek açıklamalar | Satıcıya özel bilgileri (hem kuruluşlar, hem de kişiler için) yakalamak üzere düz metin ve URL kullanan işletmeler. |
| [Satış siparişi başlığı belge ekleri](mapping-reference.md#229) | Ek açıklamalar | Satış siparişi ile ilgili bilgileri yakalamak için düz metin ve URL kullanan işletmeler. |
| [Satın alma siparişi başlığı belge ekleri](mapping-reference.md#232) | Ek açıklamalar | Satın alma siparişi ile ilgili bilgileri yakalamak için düz metin ve URL kullanan işletmeler. |

## <a name="limitations"></a>Sınırlamalar

Notlar çözümünü yükledikten sonra bunu kaldıramazsınız. 

Daha fazla bilgi için bkz. [Çift yazma eşleme başvurusu](mapping-reference.md).

