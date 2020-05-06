---
title: Ödendiğinde öde satıcı ödemeleri ayarlama ve kullanma
description: Bu konu, müşteri ödemelerini temel alarak kısmi satıcı ödemelerini serbest bırakmak için ödendiğinde öde (PWP) koşullarının nasıl oluşturulacağını açıklamaktadır.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284125"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Ödendiğinde öde satıcı ödemeleri ayarlama ve kullanma

[!include [banner](../includes/banner.md)]

Bir alt yüklenici olarak çalışmak üzere bir satıcıyı onayladığınızda, müşteriniz proje için ödeme yapana kadar satıcıya ödemeyi yapmamak isteyebilirsiniz. Bu senaryoyu desteklemek için, satıcı ile satınalma siparişini (PO) ayarladığınızda ödendiğinde öde (PWP) koşullarını ayarlayın.

Örneğin bir müşteri bir proje faturasındaki tutarı ödediğinde, satıcı faturası tutarının tümünü veya bir bölümünü ödeme için serbest bırakabilirsiniz. Satıcıya, müşteriden ilgili ödemenin belirli bir yüzdesi alındıktan sonra ödeme yapılacağını belirten PWP şartlarını ayarlayın. Bir müşteriden kısmi ödeme alırsanız, ilgili bazı satıcı faturalarını ödeme için el ile serbest bırakabilirsiniz.

Aşağıdaki örnek, PWP koşulları kullanıldığında oluşan süreci özetler.

## <a name="example"></a>Örnek

Kuruluşunuz, bir müşteriye bilgisayar başına 150,00 ABD Doları (USD) fiyatla, yazılım yüklenmiş 100 bilgisayar sağlamayı kabul eder. Daha sonra yazılımın yüklü olduğu bilgisayarları size sağlaması için bir satıcıyı işe alırsınız. Sözleşmeye göre, müşterinin kuruluşunuza ödeme yapmadan önce bilgisayarların kalitesini onaylaması gerekir. Kuruluşunuzun ilkesi, müşteri sizi ödeme yapana kadar satıcıların ödemesini bekletmektir. Bu nedenle, projeyi yüzde 100 PWP yüzdesine sahip olacak şekilde ayarlarsınız.

Satıcı, yazılımın yüklü olduğu 100 bilgisayarı, 10.000,00 ABD Dolarlık bir faturayla birlikte size gönderir. PWP koşulları projeniz için ayarlandığından, satıcıya bilgisayar alındığında ödeme yapmazsınız. Bunun yerine, 15.000,00 tutarındaki bir faturayla birlikte bilgisayarları müşteriye gönderirsiniz. Müşteri bilgisayarları inceler ve proje faturasının tam tutarını onaylar.

Müşteriden tam ödemeyi almanızdan sonra, satıcıya, satıcı faturasının toplam miktarı olan 10.000,00'i ödersiniz.

## <a name="set-up-pwp-terms-for-a-project"></a>Proje için PWP şartlarını ayarlama

Bir proje için PWP şartlarını ayarlarken, satıcıya ödeme yapmadan önce, müşterinin size proje için ödeme yapması gereken minimum tutarı yüzde olarak belirtmeniz gerekir. Eşik tutarı, proje için müşteri faturaları üzerinden otomatik olarak hesaplanır. PWP koşulları için eşik yüzdesini ayarlamak üzere bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'e gidin.
2. PWP şartlarını ayarlamak istediğiniz projeyi bulun ve açın.
3. **Satıcı sözleşmeleri** hızlı sekmesinde **Satır ekle**'yi seçin.
3. **Hesap kodu** alanında aşağıdaki seçeneklerden birini belirleyin:

    - **Tablo** – PWP koşulları tek bir satıcıya uygulanır.
    - **Grup** – PWP koşulları bir satıcı grubundaki tüm satıcılar için geçerlidir.
    - **Tümü** – PWP koşulları Tüm satıcılar için geçerlidir.

4. Önceki adımda **Tablo** veya **Grup** seçtiyseniz, **Satıcı/Satıcı grubu** alanında, PWP şartlarının uygulanacağı satıcı veya satıcı grubunu seçin. Önceki adımda **Tümü** seçeneğini belirlediyseniz, **Satıcı/Satıcı grubu** alanı düzenlenemez.
5. Projedeki satıcı için satıcı bekletme koşulları ayarlanmışsa, **Satıcı bekletme koşulları** alanında, bekletme koşullarının Kural kodunu seçin.
6. **PWP eşik yüzdesi** alanına projenin eşik yüzdesini girin. Proje için girdiğiniz yüzde, müşterinin siz satıcıya ödeme yapmadan önce ödeme yapması gereken minimum tutarı tanımlar.

## <a name="create-a-po-that-has-pwp-terms"></a>PWP koşullarını içeren bir PO oluşturma

Bir satıcıdan gelen bir faturayı deftere naklettiğinizde, satıcı PWP koşullarına tabi ise, bu koşullar satınalma siparişi satırlarında gösterilir. PWP koşullarına sahip bir PO oluşturmak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak atama** \> **Satınalma siparişleri** \> **Tüm satınalma siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin. Sonra, **Satınalma siparişi oluştur** iletişim kutusunda, gerekli bilgileri girin ve **Tamam**'ı seçin.

    Alternatif olarak, **Tüm satınalma siparişleri** liste sayfasında varolan bir satınalma siparişini açın.

4. **Satınalma siparişi** sayfasında, **Satınalma siparişi satırları** hızlı sekmesinde, satıcının satınalma siparişi satırının ayrıntılarını gözden geçirin. **Ödendiğinde öde** ödeme seçeneği otomatik olarak seçilir ve **PWP eşik yüzdesi** alanındaki değer **Projeler** sayfasındaki **PWP eşik yüzdesi** alanından otomatik olarak kopyalanır.
6. Bir satınalma siparişi satırı için satıcıya PWP koşullarını uygulamak istemezseniz, **Ödendiğinde öde** seçeneğini temizleyin. Bu durumda, Satınalma siparişi satırına ait **PWP eşik yüzdesi** alanı 0 (sıfır) olarak ayarlanır.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Müşteri ödemesini güncelleştirme ve satıcıya ödeme yapma

Bir satıcı bir projedeki çalışmasını tamamladığında ve size bir fatura gönderdiğinde, tüm proje için PWP koşullarının karşılandığını belirlemek üzere proje durumunu ve müşteri faturalarını gözden geçirmeniz gerekir. Satıcıyla ilgili PWP şartları karşılandıysa, projenin müşteri ödemelerini temel alarak, satıcı faturasındaki hangi satırlar için ödeme yapılacağını belirleyebilirsiniz. PWP koşulları karşılanmamış olsa bile satıcıya ödeme yapmaya karar verirseniz, **Ödendiğinde öde koşullu satısı faturası** sayfasında PWP koşullarını geçersiz kılabilirsiniz.

1. **Proje yönetimi ve muhasebe** \> **Sorgular ve raporlar** \> **Bekletme sorguları** \> **Ödendiğinde öde koşullu satıcı faturası**'na gidin.
2. **Ödendiğinde öde koşullu satıcı faturası** sayfasında, incelemek istediğiniz satıcı faturasını bulmak için ara alanına değerleri girin ve **Ara**'yı seçin.
3. **Satıcı faturası satırları** hızlı sekmesinde, değiştirmek istediğiniz satırları seçin.
4. **Ödendiğinde öde** koşulları fatura satırı için karşılanıyorsa, **Satıcı ödemesini serbest bırak**'ı seçin. **Ödendiğinde öde** seçeneği temizlenir ve **Ödeme için hazır** alanındaki değer **Evet** olarak değiştirilir.
