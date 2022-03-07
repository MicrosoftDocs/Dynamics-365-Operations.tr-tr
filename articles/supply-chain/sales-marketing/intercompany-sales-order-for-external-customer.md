---
title: Harici bir müşteri için şirketlerarası satış siparişi oluşturma ve faturalama
description: Bu konuda, harici bir müşteri için şirketlerarası satış siparişinin nasıl oluşturulduğu ve faturalandırıldığı açıklanmaktadır
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548579"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Harici bir müşteri için şirketlerarası satış siparişi oluşturma ve faturalama

[!include [banner](../../includes/banner.md)]

Tüzel kişilikten aynı kuruluştaki başka bir tüzel kişiye ürünün satışını kaydetmek için şirketlerarası ticareti kullanabilirsiniz.

Orijinal satış siparişini oluşturduğunuzda, şirketlerarası satıcı için otomatik olarak bir şirketlerarası satınalma siparişi oluşturabilirsiniz. Bu, şirketlerarası satıcının tüzel kişiliğinde otomatik olarak şirketlerarası satış siparişi oluşturur.

Aşağıdaki şekilde, harici bir müşteriye satış siparişi oluşturmanız ancak ürünü müşteriye teslim edebilmeniz için önce kuruluşunuzdaki farklı bir tüzel kişilikten sipariş edilmesi gerekmesi durumunda hareketlerin akışı gösterilmektedir. Bu durumda, diğer tüzel kişiliği temsil eden satıcı hesabı için bir şirketlerarası satınalma siparişi oluşturulur. Buna karşılık, tüzel kişiliğinizi temsil eden müşteri hesabı için diğer tüzel kişilikte bir şirketlerarası satış siparişi oluşturulur. Şirketlerarası satınalma siparişi faturalandırıldığında, doğrudan teslimatsa orijinal satış siparişinin faturası otomatik olarak deftere nakledilir.

![Şirketlerarası harici satış süreci](media/intercompanyexternalsalesprocess.png)

Doğrudan teslimat kullanıyorsanız ve **Fatura deftere nakil** sayfasındaki **Miktar** alanında **Sevk irsaliyesi** seçeneğini belirlerseniz şirketlerarası satıcı faturası daha önce deftere nakledilen şirketlerarası ürün girişini temel alır.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, şirketlerarası faturaları otomatik olarak deftere nakletmek ve yazdırmak için aşağıdaki önkoşulların karşılandığından emin olun.

1. **Satış ve pazarlama \> Müşteriler \> Tüm müşteriler** öğesine gidin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. **Tedarik ve kaynak \> Satıcılar \> Tüm satıcılar**'a gidin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. Satıcı veya müşteri için **Şirketlerarası** sayfasında, **Satınalma siparişi politikaları** alanında, **Şirketlerarası satınalma siparişi (doğrudan teslim)** alan grubunda **Faturayı otomatik olarak deftere naklet** onay kutusunu seçin.
1. **Satınalma siparişi politikaları** alanında, **Orijinal satış siparişi (doğrudan teslim)** alanı grubunda **Faturayı otomatik olarak deftere naklet** onay kutusunu seçin. Şirketlerarası satıcı faturasını deftere naklettiğinizde orijinal satış siparişinin faturasının otomatik olarak yazdırılmasını istiyorsanız bu onay kutusunu seçin.

> [!NOTE]
> Faturanın yazdırma ayarları, **Yazdırma yönetimi kurulumu** sayfasındaki modül, belge veya işlem kurulumuna göre belirlenir.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Harici bir müşteri için orijinal satış siparişi oluşturma

Bu adımları A tüzel kişiliğinde yapın. Bu yordam, resimde 1 etiketli kutuya karşılık gelir.

1. **Alacak hesapları \> Satış siparişi \> Tüm satış siparişleri**'sayfasına gidin.
1. **Tüm satış siparişleri** liste sayfasından, orijinal satış siparişini oluşturun. Alan değerleri, müşteri hesabından satış siparişine kopyalanır.
1. **Satış siparişi** sayfasında, Eylem Bölmesi'nde **Başlık görünümü** sayfasını seçin.
1. **Şirketlerarası ayarlar** hızlı sekmesinde, **Şirketlerarası siparişleri otomatik oluştur** onay kutusunu seçin.
1. Şirketlerarası satıcının maddeyi doğrudan harici müşteriye teslim etmesini istiyorsanız **Doğrudan teslim** onay kutusunu seçin.
1. Satış siparişini girmeyi tamamladığınızda **Satış siparişi** sayfasını kapatın.

Şirketlerarası satınalma siparişi, atanmış şirketlerarası satıcıya sahip tüm kalemler için otomatik olarak oluşturulmasının ardından şirketlerarası satış siparişi oluşturulur. Bir bilgi iletisinde, şirketlerarası satınalma siparişinin ve şirketlerarası satış siparişinin oluşturulduğu bildirilir. Mesaj ayrıca bu siparişlere bağlantılar içerir. Öğe bulunamazsa, sipariş oluşturma işleminin tamamlanmadığı anlamına gelen kırmızı bir uyarı görüntülenir.

> [!NOTE]
> Farklı tüzel kişiliklerde birkaç sipariş oluşturuyorsanız ve bu tüzel kişiliklerden birinde maddeler bulunamadıysa siparişlerini yerine getirebilecek tüzel kişilikler için bile sipariş oluşturma işlemi durur.

## <a name="invoice-an-intercompany-sales-order"></a>Şirketlerarası satış siparişini faturalandırma

Şirketlerarası satış siparişi faturalandırıldığında, karşılık gelen şirketlerarası satınalma siparişi otomatik olarak faturalandırılır. Ardından, orijinal satış siparişi, doğrudan teslimat siparişi ise orijinal satış siparişi otomatik olarak faturalandırılır.

Bu adımları B tüzel kişiliğinde yapın. Bu yordam, resimde 2 etiketli kutuya karşılık gelir.

1. **Alacak hesapları \> Satış siparişi \> Tüm satış siparişleri**'sayfasına gidin.
1. **Tüm satış siparişleri** liste sayfasında, şirketlerarası satış siparişini seçin.
1. Eylem Bölmesi'nde **Fatura** ve ardından **Fatura** sekmesini seçin.
1. **Deftere nakletme** onay kutusunu seçin.
1. Satış siparişini ve ardından **Tamam** sekmesini seçin.

Şirketlerarası satış siparişi için müşteri faturası otomatik olarak B tüzel kişiliğinde deftere nakledilir. Şirketlerarası satıcı faturası daha sonra otomatik olarak oluşturulur ve A tüzel kişiliğinde deftere nakledilir. Orijinal satış siparişi doğrudan teslimat olarak ayarlandıysa A tüzel kişiliğindeki orijinal satış siparişi için müşteri faturası oluşturulur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
