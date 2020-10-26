---
title: Uyarı kuralları oluşturma
description: Bu konu, uyarılar hakkında bilgi sağlar ve bir uyarı kuralının nasıl oluşturulacağını açıklar. Böylece, bir tarih geldiğinde veya meydana gelen belirli bir değişiklik gibi olaylar hakkında bilgilendirilirsiniz.
author: tjvass
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 94b68138066867fad641c70a1674c9292920ec6a
ms.sourcegitcommit: d540998ad6f9c894ca99498c045ae4b86b779806
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "3970691"
---
# <a name="create-alert-rules"></a>Uyarı kuralları oluşturma

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Başlarken

Uyarı kuralını ayarlamadan önce, ne zaman ve hangi durumlarda uyarı almak istediğinize karar verin. Hangi olay hakkında bilgilendirilmek istediğinizi bildiğinizde, bu olaya neden olan verilerin göründüğü sayfayı bulun. Olay, gelecek bir tarih veya meydana gelen özel bir değişiklik olabilir. Bu nedenle, tarihin belirtildiği veya değişen alanın bulunduğu ya da oluşturulan yeni kaydın göründüğü sayfayı bulmanız gerekir. Bu bilgilere sahip olduktan sonra uyarı kuralını oluşturabilirsiniz.

Uyarı kuralı oluşturduğunuzda bir uyarı tetiklenmeden önce yerine getirilmesi gereken ölçütleri tanımlarsınız. Ölçütler, olayın ortaya çıkmasıyla belirli koşulların yerine getirilmesi arasındaki eşleşmelerdir. Olay oluştuğunda sistem, ayarlanmış koşullara göre denetim gerçekleştirmeye başlar.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Uyarı toplu işlerinin çalıştığından emin olun

Uyarı koşullarının işlenmesi ve gönderilecek bildirimler için veri değişikliği ve vade tarihi uyarılarının toplu işlerinin çalışıyor olması gerekir. Toplu işleri çalıştırmak için, **sistem yönetimi** > **periyodik görevler** > **Uyarılar**'na gidin ve **değişiklik tabanlı uyarılar** ve/veya **vade tarihi uyarıları** için yeni bir toplu iş ekleyin. Uzun ve sık çalışan bir toplu iş gerekiyorsa, **tekrarlama**'yi seçin ve **dakika** cinsinden bir **tekrarlama dönemi** ve **1** **sayısı** olarak **bitiş tarihi yok** ayarlayın.

## <a name="events"></a>Olaylar

Uyarı kuralını tetikleyen olay, gelecek bir tarih veya meydana gelen belirli bir değişiklik olabilir. Olaylar için tetikleyiciler, **Uyarı kuralı oluştur** iletişim kutusunun **Beni uyarma zamanı** hızlı sekmesinde tanımlanır. Belirli bir alanda kullanılabilecek olaylar seçili tetikleyiciye bağlıdır.

Örneğin, **Başlangıç tarihi** alanı için bir uyarı kuralı ayarlıyorsanız vade tarihi olayları uygundur. Bu nedenle, bu alanda **için kalan süre** olay türü kullanılabilir. Ancak **Maliyet merkezi** gibi bir alan için bir vade tarihi olayı uygun değildir. Bu nedenle, bu alanda **için kalan süre** olay türü kullanılamaz. Bunun yerine, **değişti** olay türü kullanılabilir.

## <a name="event-types"></a>Olay tipleri

Üç tür olay gerçekleşebilir:

- **Oluşturma tipi ve silme tipi olaylar** Bu olaylar, bir kayıt oluşturulduğunda veya silindiğinde bir uyarıyı tetikler.
- **Güncelleştirme tipi olaylar**: Bu olaylar, belirli bir alandaki veriler değiştiğinde bir uyarıyı tetikler.
- **Vade tarihi tipi olaylar**: Bu olaylar, bir tarih geldiğinde bir uyarıyı tetikler.
    
Gerçekleşen değişiklikler bir kullanıcı tarafından başlatılabilir. Örneğin, bir kullanıcı bir satınalma siparişinin teslimat tarihini değiştirir. Alternatif olarak, değişiklikler bir işleminin parçası olarak gerçekleşebilir. Örneğin, bir sayfadaki **Durum** alanı sistemdeki çeşitli işlemlerin ömrünü yansıtacak şekilde değişir.

## <a name="conditions"></a>Koşullar

**Uyarı kuralı oluştur** iletişim kutusunun **Beni uyar** hızlı sekmesinde, olaylar hakkında ne zaman uyarılacağınızı denetlemek için koşullar kullanabilirsiniz.

Örneğin, sistemin sizi satınalma siparişlerinin durumu yalnızca belirli bir dizi koşulla eşleşecek şekilde değiştiğinde uyarmasını belirtebilirsiniz. Özellikle bir satınalma siparişinin durumu **Alındı** olarak değiştiğinde uyarılar almak isteyebilirsiniz. Durumdaki bu değişiklik, uyarıyı tetikleyen olaydır.

Daha sonra, hangi satınalma siparişleri hakkında uyarı almak istediğinize karar vermeniz gerekir. Örneğin, aşağıdaki seçeneklerden birini belirleyebilirsiniz. Bu seçenekler, uyarı kuralı için koşulları tanımlar.

- **Geçerli seçili kayıt**: Belirli bir satınalma siparişinin durumu **Alındı** olarak değiştiğinde uyarı alırsınız.
- **Tüm kayıtlar**: Satınalma siparişinin durumu, etkin sayfa görünümündeki bir madde için değiştiğinde uyarı alırsınız. Belirli bir kayıt kümesine ilişkin kurallar oluşturmak için sayfada bulunan gelişmiş filtrelemeyi kullanabilirsiniz. Örneğin, belirli bir müşteri grubundaki müşterilere yönelik tüm satınalma siparişleri için tetiklenen bir uyarı oluşturabilirsiniz.
    
## <a name="expiry-of-rule"></a>Kuralın sona ermesi

**Uyarı kuralı oluştur** iletişim kutusunun **Beni şu tarihe kadar uyar** hızlı sekmesinde, uyarı kuralının ne kadar süreyle etkin olacağını belirtebilirsiniz.

## <a name="alert-contents"></a>Uyarı içeriği

**Uyarı kuralı oluştur** iletişim kutusunun **Bana gönderilecek uyarı biçimi** hızlı sekmesinde, uyarı iletisinin kullanması gereken konu metnini ve ileti metnini belirtebilirsiniz.

## <a name="user-id"></a>Kullanıcı Kimliği

**Uyarı kuralı oluştur** iletişim kutusunun **Bana gönderilecek uyarı biçimi** hızlı sekmesinde, uyarı iletisini hangi kullanıcının alması gerektiğini belirtebilirsiniz. Varsayılan olarak kullanıcı kimliğiniz seçilir. Uyarıyı alan kullanıcıyı değiştirme yeteneği kuruluş yöneticilerle sınırlıdır.

## <a name="alerts-as-business-events"></a>İş olayları olarak uyarılar

Uyarılar, iş etkinlikleri çerçevesi kullanılarak harici olarak gönderilebilir. Bir uyarı oluştururken, **Organizasyon genelinde** **Hayır**'ı ayarlayın ve **harici gönder**'i **Evet** olarak ayarlayın. Uyarıyı iş olayını harekete geçirdikten sonra, bir iş olayı ile Finance and Operations bağlayıcı üzerindeki **Bir iş etkinliği olurken** tetikleyicisini kullanrak Power Automate'de yerleşik bir akışı tetikleyebilirsiniz veya iş olayları son noktasına **İş etkinlikleri kataloğu** aracılığıyla olayı açıkça gönderebilirsiniz.

## <a name="create-an-alert-rule"></a>Uyarı kuralı oluşturma

0. Uyarı toplu işlerinin çalıştığından emin olun (yukarıya bakın).
1. İzlenecek verileri içeren sayfayı açın.
2. Eylem Bölmesinde, **Seçenekler** sekmesindeki **Paylaş** grubunda **Uyarı kuralı oluştur**'u seçin.
3. **Uyarı kuralı oluştur** iletişim kutusunda **Alan** alanında, izlenecek alanı seçin.
4. **Olay** alanında, olay türünü seçin.
5. **Beni uyar** hızlı sekmesinde istenen seçenek belirleyin. Uyarıyı bir iş olayı olarak göndermek istiyorsanız, **organizasyon genelindeki** **Hayır** olarak ayarlandığından emin olun.
6. Uyarı kuralı etkinliğinin belirli bir tarihte son bulması gerekiyorsa **Beni şu tarihe kadar uyar** hızlı sekmesinde bir bitiş tarihi seçin.
7. **Bana gönderilecek uyarı biçimi** hızlı sekmesinde **Konu** alanında, e-posta iletisi için varsayılan konu başlığını kabul edin veya yeni bir konu girin. Metin, bir uyarı tetiklendiğinde aldığınız e-posta iletisinin konu başlığı olarak kullanılır. Uyarıyı bir iş olayı olarak göndermek istiyorsanız, **harici gönder**'i **Evet** olarak ayarlayın.
8. **İleti** alanına, isteğe bağlı bir ileti girin. Metin, bir uyarı tetiklendiğinde aldığınız ileti olarak kullanılır.
9. Ayarları kaydetmek ve uyarı kuralı oluşturmak için **Tamam**'a tıklayın.

## <a name="limitations-and-workarounds"></a>Sınırlamalar ve geçici çözümler

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Bir formun ikincil veri kaynakları için uyarı oluşturmaya yönelik geçici çözüm
Formlardaki bazı ikincil veri kaynakları için uyarılar oluşturulamaz. Örneğin, müşteri veya satıcı deftere nakil profilleri formunda uyarı oluştururken, boyut hesapları değil, yalnızca başlıktaki alanlar (CustLedger veya VendLedger) kullanılabilir. Bu sınırlamanın geçici çözümü, bu tabloyu birincil veri kaynağı olarak açmak üzere **SysTableBrowser** kullanmaktır. 
1. Tabloyu **SysTableBrowser** formunda açın.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. SysTableBrowser formundan bir uyarı oluşturun.

