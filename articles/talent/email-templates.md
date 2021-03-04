---
title: Attract'te e-posta şablonları oluşturma
description: Bu konu, oluşturabileceğiniz ve Microsoft Dynamics 365 Talent - Attract'te kullanabileceğiniz e-posta şablonları hakkında bilgi sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 55c12010cfd055ee6977f50e566b70f76a2e1682
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462788"
---
# <a name="create-email-templates-in-attract"></a>Attract'te e-posta şablonları oluşturma

[!include [banner](includes/banner.md)]

E-posta şablonu kitaplığı kullanarak, yöneticiler Microsoft Dynamics 365 Talent: Attract ve Offer aracılığıyla gönderilen tek tip bir tema ve tüm e-postaları için markalama oluşturabilir. Yöneticiler, diğer kullanıcıların yararlanacağı e-posta içerik şablonları koleksiyonu oluşturabilir. İşe alma ekibi, e-postaları etkili bir şekilde göndermek için bu şablonları iş akışında kullanabilir. Bazı e-postalar otomatik olarak gönderilmesi yapılandırılmış ve yönetici e-posta şablonu kitaplığını kullanarak bu e-postaların içeriğini özelleştirebilir.

> [!NOTE]
> E-posta şablonları kullanmak için kuruluşunuzun işe alma kapsamlı eklentisinin olması gerekir.

## <a name="global-template-configurations"></a>Genel şablon yapılandırmaları

Tüm e-posta iletişimi için tutarlı markalama oluşturmak için yönetici, tüm e-posta şablonları için önce genel üstbilgi ve altbilgi ayarlamalıdır. Yönetici Merkezi içinde **E-posta şablonu ayarları** sekmesindeki **Üstbilgi** bölümünde, yönetici tüm e-postalar için üstbilgi veya başlık olarak kullanmak üzere görüntü yükleyebilir. Görüntü şirket logosu, antet veya diğer tanıtım resmi olabilir. Genişliğin 25 ve 800 piksel arasında olmasını, yüksekliğin 25 ve 150 piksel arasında olmasını öneririz çünkü bu boyutlar Microsoft Outlook gibi birçok e-posta istemcisi için idealdir. Görüntü JPEG, JPG, PNG veya SVG dosyası olmalıdır ve dosya boyutu 1 megabayttan (MB) az olmalıdır. Resim karşıya yüklendikten sonra üstbilginin önizlemesi oluşturulur ve gösterilir. Üstbilgi resmi kaldırılmış veya değiştirilmişse yönetici, önizlemenin üzerindeki **Kaldır** seçeneğini kullanabilir.

**Altbilgi** bölümünde yönetici, iletişimler için şirketin gizlilik ilkesi ile şartlar ve koşullar bağlantılarını sağlar. Bu bağlantılar, otomatik olarak oluşturulan altbilgiye dahil edilir. Daha sonra bu altbilgi önizlemesi gösterilir. Yönetici ayrıca e-posta altbilgilerinde tüm e-postaların bir parçası olarak gönderilecek belirli bir dili de seçebilir. Aynı dil yapılandırması aynı zamanda görüşme özeti tablosunun bir araya getirilmesi için de kullanılacaktır. 

Yönetici Merkezi kapatmadan önce değişiklikleri kaydettiğinizden emin olun.

> [!NOTE] 
> Üstbilgi ve altbilgi tüm e-postalar için genel ayarlardır. Bu nedenle, Attract'la gönderilen tüm e-postalarda görüntülenir. Ayarları yapılandırılmamışsa üstbilgi ve altbilgi tüm e-postalar dışında bırakılır.

## <a name="email-template-library"></a>E-posta şablonu kitaplığı 

Genel şablon konfigürasyonları ayarlandıktan sonra yönetici, Attract and Offer'dan gönderilen tüm e-posta şablonlarını oluşturma ve yönetmeye başlayabilir. E-posta şablonu kitaplığı yalnızca yöneticiler için kullanılabilir. Ana gezinti menüsünden kitaplığı açmak için **E-posta şablonları** sekmesini seçin. Kitaplık, planlama, değerlendirme ve iş oluşturma ve teklifi gibi e-postaların gönderme amacıyla Attract'teki çeşitli faaliyetlerle kategorilere ayrılmıştır. Yönetici, faaliyetle ilişkili olan tüm e-posta türlerini görüntülemek için herhangi bir kategoriyi seçebilir. Örneğin, planlama işlemi sırasında gönderilen çeşitli e-postaları ve her e-posta türü için mevcut olan şablonları görüntülemek için **Planlama**'yı seçin. Bir kategoride her alt bölüm bir tür e-postayı temsil eder.

Bazı e-posta türleri birden çok alıcı içerebilir. Örneğin, **Planlama** kategorisinde, görüşme çizelgesi özeti gerekli olduğunda gönderilen e-postalar hem adaylara hem görüşmecilere gönderilir. Her bölümün ana iki sütunu vardır: **Şablon başlığı** ve **Alıcı**. Bir bölümdeki her satır, bir e-posta türünü temsil eder. Başlangıçta, her şablon için satırda bir kilit simgesi görüntülenir. Bu simge, şablonun Attract'te sağlanan standart şablon olduğunu ve silinemez olduğunu gösterir. Her şablon için yönetici, üç nokta düğmesini (**...**) kullanarak şablonu yineleyebilir, varsayılan şablon olarak ayarlayabilir veya silebilir. Bir şablon varsayılan şablon olarak ayarlandığında, iki davranıştan biri oluşabilir. Şablonun satırında gösterilen rozet veya rozetler davranışı belirtir:

- **Varsayılan** – Bu rozet, gönderilen e-posta şablonunun varsayılan şablon olduğunu gösterir ve bilgilerin, kullanıcı belirli türdeki e-posta gönderince gireceğini belirtir.
- **Varsayılan** + **Oto. gönder** – Bu rozetler birleşimi, şablonun otomatik olarak gönderilecek sistem tarafından oluşturulan e-posta şablonunun etkin olduğunu gösterir.

Bir şablonu düzenlemek için satırı seçin ve şablonda değişiklikler yapın.

> [!NOTE]
> Belirli türdeki e-postanın her bir alıcısı varsayılan şablona sahiptir. Tüm standart Attract şablonları, yönetici e-posta belirli bir tür için yeni bir şablon oluşturuncaya ve varsayılan şablon olarak ayarlayıncaya kadar varsayılan şablon olarak ayarlanır.

## <a name="create-a-template"></a>Şablon oluştur

Şablon oluşturmak için e-posta şablonu kitaplığınınsağ üst köşesinde **+ Yeni şablon** u seçin. Şablonu oluşturmakta olduğunuz e-posta türünü seçmek için alıcı, işlem ve e-posta gönderilmesi için bir olay seçin. Ardından **Oluştur**'u seçin.

Şablon düzenleme görünümünde açılır ve şablonu adlandırabilirsiniz. Örneğin, şablon ABD ünivertsitesi adayları içindir, ancak içerik Fransızca yazılmıştır, bu durumda başlık olarak **Üniversite\_ABD\_Francais** girin. Her şablonun başlık, konu satırı ve gövde içeriği İngilizce dışındaki dillerle de destekleyebilir.

Şablonun **Kime** alanı düzenlenemez çünkü şablonu oluşturduğunuzda alıcı seçilmiştir.

Bilgi (Cc) satırına **İş veren** veya **İşe alma yöneticisi** gibi kişiler ekleyebilirsiniz. E-posta gönderildiğinde, bu roller kullanıcılarla işin bağlamını temel alarak uygun kullanıcılarla otomatik olarak değiştirilir.

Konu satırı ve gövde içeriği yer tutucuları destekler. **\#** yazarak ve otomatik tamamlanan açılır listeden uygun yer tutucu seçerek yer tutucu ekleyebilirsiniz. Kullanılabilir yer tutucular listesi sayfanın sağ tarafında görünür. E-posta gönderildiğinde, yer tutucular işin bağlamını ve alıcıyı temel alarak uygun kullanıcılarla otomatik olarak değiştirilir. Örneğin, adaya gönderilen e-posta şablonu yer tutucu içerir \#{Aday\_Ad}. Cameron adlı bir adaya e-posta gönderildiğinde bu yer tutucu olan Cameron'ın adı ile değiştirilir.

Gövde içerik düzenleyici, stil ve formatı sağlayan zengin metin düzenleyicisidir. Ayrıca, köprüler ve bağlantılar eklemenizi sağlar.

Belirli bir e-posta tipi için bir şablon oluşturulduktan sonra şablon satırıındaki üç nokta düğmesini (**...**) seçin ve varsayılan şablon olarak ayarlayın.

## <a name="consume-templates"></a>Şablonları kullanın

İşe alma ekibi e-posta gönderirken yöneticinin oluşturduğu şablonları kullanabilirsiniz. E-posta için birden çok şablon oluşturulursa e-posta bileşim iş akışında açılır liste görünür. Varsayılan şablon otomatik olarak girilir, ancak kullanıcı farklı bir şablon seçebilir.

> [!NOTE] 
> Otomatik olarak gönderilen e-postalar için birden çok şablon oluşturulabilir. Bununla birlikte, tek bir şablon etkin şablon olarak ayarlanabilir. Bu süreç olaylarla tetiklendiğinden yalnızca yönetici, şablon kitaplığındaki **varsayılan** ve **Oto. gönder** rozetleri bileşimine bağlı olarak hangi şablonun kullanılması gerektiğini belirleyebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]