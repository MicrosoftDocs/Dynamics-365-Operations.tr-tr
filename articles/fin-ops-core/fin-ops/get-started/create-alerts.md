---
title: Uyarı kuralları oluşturma
description: Bu konu, uyarılar hakkında bilgi sağlar ve bir uyarı kuralının nasıl oluşturulacağını açıklar. Böylece, bir tarih geldiğinde veya meydana gelen belirli bir değişiklik gibi olaylar hakkında bilgilendirilirsiniz.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
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
ms.openlocfilehash: c37ddc52ef576a15dd35cc155e99821c74631a46
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180726"
---
# <a name="create-alert-rules"></a>Uyarı kuralları oluşturma

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Başlarken

Uyarı kuralını ayarlamadan önce, ne zaman ve hangi durumlarda uyarı almak istediğinize karar verin. Hangi olay hakkında bilgilendirilmek istediğinizi bildiğinizde, bu olaya neden olan verilerin göründüğü sayfayı bulun. Olay, gelecek bir tarih veya meydana gelen özel bir değişiklik olabilir. Bu nedenle, tarihin belirtildiği veya değişen alanın bulunduğu ya da oluşturulan yeni kaydın göründüğü sayfayı bulmanız gerekir. Bu bilgilere sahip olduktan sonra uyarı kuralını oluşturabilirsiniz.

Uyarı kuralı oluşturduğunuzda bir uyarı tetiklenmeden önce yerine getirilmesi gereken ölçütleri tanımlarsınız. Ölçütleri, olayın ortaya çıkmasıyla belirli koşulların yerine getirilmesi arasındaki eşleşme olarak da düşünebilirsiniz. Olay oluştuğunda sistem, ayarlanmış koşullara göre denetim gerçekleştirmeye başlar.

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

**Uyarı kuralı oluştur** iletişim kutusunun **Bana gönderilecek uyarı biçimi** hızlı sekmesinde, uyarı iletisini hangi kullanıcının alması gerektiğini belirtebilirsiniz. Varsayılan olarak kullanıcı kimliğiniz seçilir. Bu seçenek, kuruluş yöneticileriyle sınırlıdır.

## <a name="create-an-alert-rule"></a>Uyarı kuralı oluşturma

1. İzlenecek verileri içeren sayfayı açın.
2. Eylem Bölmesinde, **Seçenekler** sekmesindeki **Paylaş** grubunda **Uyarı kuralı oluştur**'u seçin.
3. **Uyarı kuralı oluştur** iletişim kutusunda **Alan** alanında, izlenecek alanı seçin.
4. **Olay** alanında, olay türünü seçin.
5. **Beni uyar** hızlı sekmesinde bir seçenek belirleyin.
6. Uyarı kuralı etkinliğinin belirli bir tarihte son bulması gerekiyorsa **Beni şu tarihe kadar uyar** hızlı sekmesinde bir bitiş tarihi seçin.
7. **Bana gönderilecek uyarı biçimi** hızlı sekmesinde **Konu** alanında, e-posta iletisi için varsayılan konu başlığını kabul edin veya yeni bir konu girin. Metin, bir uyarı tetiklendiğinde aldığınız e-posta iletisinin konu başlığı olarak kullanılır.
8. **İleti** alanına, isteğe bağlı bir ileti girin. Metin, bir uyarı tetiklendiğinde aldığınız ileti olarak kullanılır.
9. Ayarları kaydetmek ve uyarı kuralı oluşturmak için **Tamam**'a tıklayın.
