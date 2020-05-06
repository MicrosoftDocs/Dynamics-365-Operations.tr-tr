---
title: Proje verme
description: Bu konu bir vermenin nasıl oluşturulacağını veya değiştirileceğini açıklar.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282854"
---
# <a name="project-grants"></a>Proje verme

[!include [banner](../includes/banner.md)]

Verme, belirli bir amaç veya proje için bir para hediyesidir. Genellikle, bir vermenin nasıl harcanacağıyla ilgili kısıtlamalar vardır. Proje yönetimi ve muhasebede, verme işlemlerini girebilir ve izleyebilir ve bunların proje ve proje sözleşmeleriyle ilişkilerini tanımlayabilirsiniz. Örneğin aşağıdaki görevleri gerçekleştirebilirsiniz:

- **Proje** ve **Proje sözleşmesi ayrıntıları** sayfalarına bağlantılar yoluyla, vermeleri projeler ve finansman kaynaklarıyla ilişkilendirmek.
- Bir durumdan diğerine taşındığında, vermede yapılan değişiklikleri girmek ve izlemek.
- Maliyetleri, talep edilen tutarları ve verilen tutarları girmek ve izlemek.
- Ana vermeler oluşturmak ve alt vermeleri bunlarla ilişkilendirmek.

Tüm ayrıntıları yeni bir kayda girerek bir verme oluşturabilir veya varolan bir vermeden alınan ayrıntıları kopyalayabilir ve onları güncelleştirebilirsiniz.

## <a name="create-a-new-grant"></a>Yeni bir verme oluştur

1. **Proje yönetimi ve muhasebeyle** \> **Vermeler** \> **Vermeler**'e gidin.
2. **Yeni** \> **Verme**'yi seçin.
3. Verme ayrıntıları sayfasında **Genel** hızlı sekmesinde, **Verme kodu** alanında, verme için alfasayısal bir tanımlayıcı girin.
4. **Verme adı** alanına verme için benzersiz bir ad girin.
5. **Açıklama** alanına, yeni verme ile ilgili ayrıntıları ekleyin.

    Sayfadaki diğer alanların çoğu isteğe bağlıdır ve istediğiniz kadar çok veya az bilgi girebilirsiniz.

    Aşağıdaki listede, her verme ayrıntıları sayfası hızlı sekmesinde belirtilen bilgiler açıklanmaktadır:

    - **Genel** – Verme adını, durumunu, açıklamasını, amacını ve tutarını girin.
    - **İlgili kişi bilgileri** – Personel üyeleriyle ilgili ayrıntıları, vermeyi yöneten departmanı ve verme için müşteri ya da kuruluş verme kaynağını girin. Ayrıca, organizasyonunuzun, verme alan ve daha sonra başka bir alıcıya aktaran bir geçiş varlığı olup olmadığını da belirtebilirsiniz. Vermeyi sağlayan kuruluşun telefon numaraları ve e-posta adresleri gibi kişi bilgilerini eklemek için **Ekle**'yi seçin.
    - **Tarihler ve son tarihler** – Verme ve verme uygulamasıyla ilgili tarihleri girin. Örnekler arasında uygulama son tarihi, gönderme tarihi ve vermenin onaylandığı veya reddedildiği tarih bulunur.
    - **İlişkili projeler ve proje sözleşmeleri** – Bu hızlı sekmede yalnızca **Genel** hızlı sekmesinin **Verme durumu** **Etkin** veya **Verildi** olarak ayarlanmışsa bilgi girebilirsiniz. İlgili görevi tamamlamak için aşağıdaki seçenekler arasından seçim yapın:

        - **Finansman kaynağı ekle** – Verme için yeni bir finansman kaynağı ekleyin. Tüm ayrıntıları şimdi girebilir veya varsayılan bilgileri kullanıp daha sonra güncelleştirebilirsiniz.
        - **Proje sözleşmesi ekle** - Proje sözleşme bilgilerini ekleyin veya güncelleştirin.
        - **Proje ekle** – Proje ayrıntılarını ekleyin veya güncelleştirin.

    - **Kurulum** – Bu bilgiler gerekiyorsa, eşleşen fonların ayrıntılarını girin. Verme sunan kuruluşların çoğu, alıcıların verme ile sunulan tutarla eşleşmek üzere, kendi para veya kaynaklarını belirli bir miktarda harcamalarını gerektirir. **Yerel proje veya izleme kimliği** alanında, proje tanımlayıcısından farklı bir tanımlayıcı girebilirsiniz.

        > [!NOTE]
        > Vermenin bir kısmı farklı bir kuruluşa verilecekse, **Alt veren** seçeneğini **Evet** olarak ayarlayın. Amerika Birleşik Devletleri'nde sağlanan vermelere yönelik olarak, vermenin bir eyalet yönergesi veya federal yönerge altında mı gerçekleştirileceğini belirtebilirsiniz.

    - **Düşüm ayrıntıları** – Verilen fonların ne sıklıkla geri alınacağına, faturalanacağına veya harcanabileceğine ilişkin bilgileri ekleyin veya güncelleştirin.

## <a name="create-a-new-grant-from-a-copy"></a>Kopyadan yeni verme oluşturma

1. **Proje yönetimi ve muhasebeyle** \> **Vermeler** \> **Vermeler**'e gidin.
2. **Yeni** \> **Vermeden kopyala**'yı seçin.
3. Yeni verme için alfasayısal bir tanımlayıcı ve ad girin ve **Tamam**'ı seçin.
4. Verme ayrıntıları sayfasında, kopyalanan verme ile ilgili ayrıntıları gözden geçirin ve gerekli değişiklikleri yapın. Sayfadaki alanların çoğu isteğe bağlıdır.

## <a name="view-or-modify-grant-details"></a>Verme ayrıntılarını görüntüleme veya değiştirme

1. **Proje yönetimi ve muhasebeyle** \> **Vermeler** \> **Vermeler**'e gidin.
2. Değiştirilecek vermeyi seçin.
3. Eylem Bölmesinde, **Verme** sekmesindeki **Koru** gurubunda **Düzenle**'yi seçin.
4. Verme ayrıntılarını gözden geçirin ve gerekli değişiklikleri yapın.
