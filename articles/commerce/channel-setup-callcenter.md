---
title: Çağrı merkezi kanalı ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b25626dafc07d576699ceba3cc9ca691db45cb9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997762"
---
# <a name="set-up-a-call-center-channel"></a>Çağrı merkezi kanalı ayarlama


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir çağrı merkezi kanalının nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Özet


Dynamics 365 Commerce'te çağrı merkezi, uygulamada tanımlanabilen bir Commerce kanalı türüdür. Çağrı merkezi varlıklarınız için bir kanal tanımlamak, sistemin belirli verileri ve sipariş işleme varsayılanlarını satış siparişlerine bağlamasına olanak sağlar. Bir şirket Commerce'ta çok sayıda çağrı merkezi kanalı tanımlayabilmesine karşın, tek bir kullanıcının yalnızca tek bir çağrı merkezi kanalına bağlanabileceği unutulmamalıdır. 

Yeni bir çağrı merkezi kanalı oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.

## <a name="create-and-configure-a-new-call-center-channel"></a>Yeni bir çağrı merkezi kanalı oluşturma ve yapılandırma

Yeni bir çağrı merkez kanalı oluşturmak ve yapılandırmak için bu adımları izleyin.

1. Gezinti bölmesinde, **Retail ve Commerce \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ad** alanına yeni kanal için bir ad girin.
1. Açılır listeden uygun **Tüzel kişiliği** seçin.
1. Açılır listeden uygun **Ambar** yerleşimini seçin. Müşteri veya madde düzeyinde başka varsayılanlar tanımlanmadıkça, bu yerleşim bu çağrı merkezi kanalı için oluşturulan satış siparişlerinde varsayılan olarak kullanılacaktır.
1. **Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin. Bu veriler, yeni müşteri kayıtları oluşturulurken varsayılanları otomatik olarak doldurma işlemine yardımcı olmak üzere kullanılır. Çağrı merkezi siparişleri oluştururken, varsayılan müşteri için sipariş oluşturmanız önerilmez.
1. **E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin. Çağrı merkezi siparişleri oluşturulup işlendiğinde, e-posta bildirim profili otomatik e-posta uyarılarını müşterilere sipariş durumları hakkında bilgi verecek şekilde tetikleyebilmek için kullanılır.
1. Bir **Fiyat geçersiz kılma** bilgi kodu belirtin. Bunun için önce bir bilgi kodu oluşturmanız gerekebilir. Bu bilgi kodu, bir çağrı merkezi siparişinde fiyat geçersiz kılma işlevi kullanılırken kullanıcıdan aralarından seçim yapması istenecek bir neden kodları kümesi sağlar.
1. Bir **Tutma kodu** bilgi kodu belirtin. Bunun için önce bir bilgi kodu oluşturmanız gerekebilir. Bu bilgi kodu, beklemede bir sipariş düzenlerken kullanıcıdan aralarından seçim yapması istenecek isteğe bağlı neden kodları kümesi sağlar.
1. Bir **Kredi** bilgi kodu belirtin. Bunun için önce bir bilgi kodu oluşturmanız gerekebilir. Bu bilgi kodu, kullanıcının müşteri hizmetleri nedenleriyle müşteriye sair para iadeleri sağlamak amacıyla çağrı merkezinin sipariş alacak işlevini kullanırken aralarından seçim yapılabileceği neden kodları kümesi sağlar.
1. İsteğe bağlı: **Mali boyutlar** hızlı sekmesinde mali boyutları ayarlayın. Buraya girilen boyutlar, bu çağrı merkezi kanalında oluşturulan herhangi bir satış siparişinde varsayılan olarak yer alır.
1. **Kaydet**'e tıklayın.

Aşağıdaki resimde yeni bir çağrı merkezi kanalının oluşturulması gösteriliyor.

![Yeni çağrı merkezi kanalı](media/channel-setup-callcenter-1.png)

Aşağıdaki resimde örnek bir çağrı merkezi kanalı gösteriliyor.

![Örnek çağrı merkezi kanalı](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Ek kanal ayarları

Çağrı merkezi kanalı kurulumu için gereken ek görevler ödeme yöntemlerini ve teslimat şekillerini ayarlamayı içerir.

Aşağıdaki resimde, **Kurulum** sekmesindeki **Teslimat şekilleri** ve **Ödeme yöntemleri** ayarlama seçenekleri gösterilmektedir.

![Ek çağrı merkezi kanal kurulumu eylemleri](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Ödeme yöntemlerini ayarlama

Ödeme yöntemleri ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin. Kullanıcıların çağrı merkezi kanalına bağlanması için önceden tanımlanmış ödeme yöntemleri arasından seçim yapması istenir. Çağrı merkezi ödeme yöntemlerinizi ayarlamadan önce **Retail ve Commerce \> Kanal kurulumu \> Ödeme yöntemleri \> Ödeme yöntemleri** altında ana ödeme yöntemlerinizi ayarlayın.

1. Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. Gezinti bölmesinde, kullanılabilir önceden tanımlanmış ödemelerden bir ödeme yöntemi seçin.
1. Ödeme türü için gereken ek ayarları yapılandırın. Kredi kartları, hediye kartları veya bağlılık programı kartları için **Kart kurulumu** işlevi seçilerek ek kurulum yapılması gerekir. 
1. Ödeme türü için uygun deftere nakil hesaplarını **Deftere nakil** bölümünde yapılandırın.
1. Eylem bölmesi'nde, **Kaydet** öğesine tıklayın.

Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.

![Örnek ödeme yöntemleri](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Teslimat şekillerini ayarla

Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.  

Çağrı merkezi kanalıyla ilişkilendirilecek bir teslimat modu eklemek veya değiştirmek için aşağıdaki adımları izleyin.

1. Çağrı merkezi teslimat şekilleri formunda, **Teslimat şekillerini yönet**'i seçin
1. Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.
1. **Perakende kanalları** bölümünde, çağrı merkezi kanalı eklemek için **Satır ekle**'ye tıklayın. Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.
1. Teslimat şeklinin **Ürünler** hızlı sekmesi ve **Adresler** hızlı sekmesindeki verilerle yapılandırıldığından emin olun. Teslimat şekli için herhangi bir ürün veya teslimat adresi geçerli değilse, sipariş girişi sırasında bunu seçmek hatalara neden olur.
1. Çağrı merkezi teslimat şekli yapılandırmalarında herhangi bir değişiklik yapıldıktan sonra, değişiklik matrisini açmak için **Teslimat şekillerini işle** işi çalıştırılmalıdır. Bu işi **Retail ve Commerce \> Retail ve Commerce BT \>Teslimar şekillerini işle**'ye giderek bulabilirsiniz.

Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.

![Teslimat şekillerini ayarla](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Kanal kullanıcıları ayarlama

Commerce Headquarters'dan çağrı merkezi kanalına bağlanan bir satış siparişi oluşturmak için satış siparişini oluşturan kullanıcının çağrı merkezi kanalına bağlanması gerekir. Kullanıcı, Commerce Headquarters'da oluşturulan bir satış siparişini çağrı merkezi kanalına el ile bağlayamaz. Bağlantı sistematik bir şekilde yapılır ve kullanıcıyı ve kullanıcının çağrı merkezi kanalıyla olan ilişkisini temel alır. Bir kullanıcı yalnızca bir çağrı merkezi kanalına bağlanabilir.

1. Eylem bölmesinde, **Kanal** sekmesini ve ardından **Kanal kullanıcıları**'nı seçin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. Bu kullanıcıyı çağrı merkezi kanalına bağlamak için açılır seçim listesinden mevcut bir **kullanıcı kimliği** seçin

Kanal kullanıcısı ayarı yapıldıktan ve kullanıcı Commerce Headquarters'da yeni bir satış siparişi oluşturduktan sonra, satış siparişi oluşturan kullanıcının ilişkili çağrı merkezi kanalına bağlanır. Bu kanalla ilgili tüm yapılandırmalar sistematik olarak satış siparişine uygulanacaktır. Bir kullanıcı satış siparişi başlığındaki kanal adı referansını görüntüleyerek satış siparişinin hangi çağrı merkezi kanalına bağlandığını onaylayabilir.


### <a name="set-up-price-groups"></a>Fiyat grupları ayarlama

Fiyat grupları isteğe bağlıdır, ancak kullanılması durumunda, çağrı merkezi kanalında sipariş veren müşterilere hangi satış fiyatlarının sunulacağını kontrol edilebilir. Müşteri için bir fiyat grubu yapılandırılmamış veya katalog fiyat grupları satış siparişine uygulanmamışsa (çağrı merkezi sipariş başlığındaki **Kaynak kod kimliği** alanını kullanarak), madde fiyatlarını bulmak için kanal fiyat grubu kullanılır. Çağrı merkezi kanalında bir fiyat grubu bulunamazsa, varsayılan madde ana fiyatları kullanılır. 

Fiyat grubu ayarlamak için aşağıdakileri yapın.

1. Eylem bölmesinde, **Kanal** sekmesine ve ardından **Fiyat grupları**'na tıklayın.
1. Eylem bölmesinde **Yeni**'ye tıklayın.
1. Açılır seçim listesinden bir **Perakende fiyat grubu** seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Çağrı merkezi satış işlevi](call-center-functionality.md)

[Çağrı merkezi sipariş işleme seçeneklerini ayarlama](set-up-order-processing-options.md)

[Çağrı merkezi katalogları](call-center-catalogs.md)

[Sahtekarlık uyarılarını ayarlama ve bunlarla çalışma](set-up-fraud-alerts.md)

[Çağrı merkezleri için süreklilik programları ayarlama](set-up-continuity-program.md)
