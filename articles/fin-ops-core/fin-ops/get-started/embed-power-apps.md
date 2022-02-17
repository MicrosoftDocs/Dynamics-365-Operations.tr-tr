---
title: Power Apps uygulamasından tuval uygulamalarını ekleme
description: Bu konu ürün işlevselliğini artırmak için Microsoft Power Apps uygulamasından tuval uygulamalarının istemciye nasıl katıştırılacağını açıklar.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: c2f7b660d364be6e62d484e67908201027190a8a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065131"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Apps uygulamasından tuval uygulamalarını ekleme

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps, geliştiricilerin ve teknik olmayan kullanıcıların mobil cihazlar, tabletler ve web için kod yazmak zorunda kalmadan özel iş uygulamaları oluşturmalarına olanak tanır. Finans ve Operasyon uygulamaları, Power Apps ile tümleştirmeyi destekler. Sizin, kuruluşunuzun veya daha geniş ekosistemin geliştirdiği tuval uygulamaları, ürünün işlevselliğini artırmak için Finans ve Operasyon uygulamalarına gömülebilir. Örneğin, başka bir sistemden alınan bilgilerle bir Finans ve Operasyon uygulamasını desteklemek için Power Apps'ten bir tuval uygulaması oluşturabilirsiniz.

Katıştırılmış tuval uygulamaları hakkında daha fazla bilgi için [Tuval uygulamalarını katıştırma](https://www.youtube.com/watch?v=x3qyA1bH-NY) kısa videosunu izleyin.

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Power Apps'ten bir sayfaya katıştırılmış bir tuval uygulaması ekleme

İstemciye Power Apps'ten bir tuval uygulaması katıştırmadan önce, istediğiniz görsellere ve/veya işleve sahip bir uygulama bulmanız veya oluşturmanız gerekir. Bu konu, uygulama oluşturma işleminin ayrıntılı açıklamasını içermez. Power Apps uygulamasında yeni iseniz, [Power Apps belgelere](/powerapps/) bakın.

Bir tuval uygulamasını Finans ve Operasyon uygulamasına katıştırmanın üç yolu vardır. Senaryonuza en uygun yaklaşımı kullanabilirsiniz. 

- Tuval uygulamasını, bir sayfanın standart Eylem Bölmesi'ndeki **Power Apps** düğmesine katıştırın. Bu şekilde eklediğiniz uygulamalar **Power Apps** menü düğmesinde maddeler olarak görünür ve uygulamalar yan bölmelerde açılır. 
- Tuval uygulamasını doğrudan yeni sekme sayfası (pivot sekmesi, hızlı sekme, dikey pencere veya çalışma alanı bölümü) olarak mevcut bir sayfaya katıştırın.
- Panodan tuval uygulaması için yeni bir tam sayfa deneyimi oluşturun.

Katıştırılmış tuval uygulamanızı yapılandırırken, uygulamaya bağlam olarak göndermek istediğiniz tek bir alan seçebilirsiniz. Bu adın uygulamanın görüntülemekte olduğunuz verilere dayanarak yanıt vermesini sağlar.

> [!NOTE]
> Model temelli uygulamaları katıştırmak için bu mekanizmayı kullanamazsınız.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Mevcut bir sayfaya tuval uygulaması katıştırma

Aşağıdaki yordamda, tuval uygulamasının Power Apps'ten mevcut bir sayfaya nasıl katıştırılacağı gösterilmektedir.

1. Tuval uygulamasını katıştırmak istediğiniz sayfaya gidin. Bu sayfa, uygulamaya giriş olarak geçirilmesi gereken tüm verileri içerir.
2. **Power Apps'ten bir uygulama ekle** bölmesini açın:

    - Uygulama doğrudan sayfaya katıştırılacaksa **Seçenekler** \> **Bu sayfayı kişiselleştir** \> **Daha fazla**'yı seçin ve ardından şu adımlardan birini izleyin:

        - **Tam sayfa uygulamalar** özelliği açıksa **Sayfa ekle**'yi seçin ve ardından uygulamayı eklemek istediğiniz bölgeyi seçin. Uygulamayı **Power Apps** menü düğmesine katıştırmak için Eylem Bölmesi'ni seçin. Uygulamayı doğrudan sayfaya katıştırmak için uygun sekmeyi, hızlı sekmeyi, dikey pencereyi veya bölümü (bir çalışma alanındaysanız) seçin. Ardından, **Bir uygulama ekle** bölmesinde **Power Apps**'i seçin.
        - **Tam sayfa uygulamalar** özelliği kapalıysa **Power Apps'ten uygulama ekle** seçeneğini belirleyin ve ardından uygulamayı eklemek istediğiniz bölgeyi seçin. Uygulamayı **Power Apps** menü düğmesine katıştırmak için Eylem Bölmesi'ni seçin. Uygulamayı doğrudan sayfaya katıştırmak için uygun sekmeyi, hızlı sekmeyi, dikey pencereyi veya bölümü (bir çalışma alanındaysanız) seçin.

    - Uygulamaya **Power Apps** menü düğmesi kullanılarak erişilecekse standart Eylem Bölmesi'nde **Power Apps** menü düğmesini ve ardından **Uygulama ekle**'yi seçebilirsiniz.

3. Katıştırılmış uygulamayı yapılandırın. Daha fazla bilgi için bu konu başlığının ilerleyen bölümlerinde yer alan [Tuval uygulamasını yapılandırma](#configuring-a-canvas-app) bölümüne bakın.
4. Yapılandırmanın doğru olduğunu onayladıktan sonra **Ekle**'yi seçin.

    - **Kayıtlı görünümler** özelliği kapalıysa katıştırılmış uygulamayı görmek için tarayıcıyı yenilemeniz istenir.
    - **Kayıtlı görünümler** özelliği açıksa değişikliğin kalıcı olması için görünümü kaydetmeniz gerekir.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Panodan tuval uygulamasını tam sayfa deneyimi olarak katıştırma

Uygulama mevcut bir sayfayla ilgili değilse veya uygulamayı Finans ve Operasyon uygulamasında tam sayfa bir deneyim olarak ortaya çıkarmak istiyorsanız panodan bir tuval uygulaması katıştırmak isteyebilirsiniz.

> [!NOTE]
> Bu yeteneği kullanılabilir hale getirmek için Özellik yönetiminde **Tam sayfa uygulamalar** özelliğini açmalısınız. 

1. Panoyu açın.
2. Sayfayı seçin ve basılı tutun (veya sağ tıklayın), **Kişiselleştir**'i seçin ve ardından **Sayfa ekle**'yi seçin.
3. **Sayfa ekle** bölmesinde, **Power Apps**'i seçin.
4. Katıştırılmış uygulamayı yapılandırın. Daha fazla bilgi için bu konu başlığının ilerleyen bölümlerinde yer alan [Tuval uygulamasını yapılandırma](#configuring-a-canvas-app) bölümüne bakın.
5. Uygulamayı panoya yeni bir kutucuk olarak eklemek için **Kaydet**'i seçin.
6. Panodaki yeni kutucuğu seçin ve tuval uygulamasının beklendiği gibi görüntülendiğini onaylayın.

### <a name="configuring-a-canvas-app"></a>Tuval uygulamasını yapılandırma

Tuval uygulamasını katıştırdığınızda, aşağıdaki parametreleri ayarlamanız gerekir:

- **Ad**: Katıştırılmış uygulamayı içeren düğme veya sekme için gösterilmesi gereken metni girin. Genellikle, bu alanda uygulamanın adını tekrar etmek isteyebilirsiniz.
- **Uygulama kodu**: Katıştırmak istediğiniz tuval uygulaması için genel benzersiz tanımlayıcıyı (GUID) belirtin. Bu değeri almak için [make.powerapps.com](https://make.powerapps.com) adresinde uygulamayı bulun ve **Ayrıntılar** altından **Uygulama Kimliği** alanını bulun.
- **Uygulama için giriş bilgisi**: İsteğe bağlı olarak uygulamaya geçirmek istediğiniz verileri içeren alanı seçebilirsiniz. Uygulamanın Finans ve Operasyon uygulamalarından gönderilen verilere nasıl erişebileceği hakkında bilgi için bu konunun sonraki bölümlerinde yer alan [Finans ve Operasyon uygulamalarından gönderilen verilerden yararlanan bir uygulama oluşturma](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) bölümüne bakın.

    Sürüm 10.0.19 itibarıyla, geçerli tüzel kişilik aynı zamanda **cmp** URL parametresi aracılığıyla tuval uygulamasına bağlam olarak geçirilir. Bu davranış, söz konusu uygulama bu bilgileri kullanana kadar hedef tuval uygulamasını etkilemez.

- **Uygulama boyutu**: Katıştırdığınız uygulama türünü seçin. Mobil cihazlar için oluşturulan uygulamalar için **İnce**'yi veya tabletler için oluşturulan uygulamalar için **Geniş**'i seçin. Bu parametre, katıştırılmış uygulama için yeterli alan ayrılmasını sağlar.
- **Tüzel kişilikler**: Uygulamanın kullanılabilir olması gereken tüzel kişilikleri seçebilirsiniz. Varsayılan olarak, uygulama tüm tüzel kişilikler için kullanılabilir. Bu seçenek yalnızca var olan bir sayfaya doğrudan katıştırdığınızda ve **[Kayıtlı görünümler](saved-views.md)** özelliği kapalıysa kullanılabilir.

## <a name="sharing-an-embedded-app"></a>Katıştırılmış bir uygulamayı paylaşma

Sayfaya bir tuval uygulamasını katıştırıldıktan ve düzgün çalıştığını onayladıktan sonra, uygulamayı sistemdeki diğer kullanıcılarla paylaşmak isteyebilirsiniz. Katıştırılmış bir tuval uygulamasını paylaştırmak için, aşağıdaki adımları izleyin.

1. Kullanıcıların tuval uygulamasına doğrudan Power Apps'ten erişebilmeleri için uygun kullanıcılarla [Tuval uygulamasını Power Apps'te paylaşın](/powerapps/maker/canvas-apps/share-app).
2. Katıştırılmış uygulamayla ilişkilendirilmiş kişiselleştirmeleri istenen kullanıcılarla paylaşın. Aşağıdaki yaklaşımlardan herhangi birini kullanabilirsiniz:

    - **Görünümü yayımlayın (Önerilen):** **[Kaydedilmiş görünümler](saved-views.md)** özelliği açıksa önerilen ve tercih edilen yaklaşım katıştırılmış tuval uygulamasını içeren bir görünüm oluşturup bu görünümü istenen kullanıcılara yayımlamaktır. Bu yaklaşım, yayımlanmış görünüm tarafından hedeflenen güvenlik rollerine sahip tüm kullanıcıların sayfada tuval uygulamasını görmesini sağlar.

        Ayrıca katıştırılmış bir tuval uygulamasını panodan bir tam sayfa deneyimi olarak da yayımlayabilirsiniz. Panoda, uygulamayla ilişkilendirilmiş kutucuğu seçin ve tutun (veya sağ tıklayın), **Kişiselleştir**'i seçin ve ardından **Sayfayı yayımla**'yı seçin. *Yayımlama görünümleri* deneyimine benzer bir deneyim gösterilir ve yayımlamak için güvenlik rollerini seçebilirsiniz. 10.0.21 veya sonraki güncelleştirmede, **Kaydedilmiş görünümler için geliştirilmiş tüzel kişilik desteği** özelliği açıksa uygulamayı istediğiniz tüzel kişiliklere de yayımlayabilirsiniz.

    - **Kayıtlı görünümler** özelliği kapalıysa sistem yöneticisi **Kişiselleştirme** sayfası aracılığıyla uygun kullanıcı kümesine tuval uygulamasını içeren bir kişiselleştirme verebilir. Alternatif olarak, sayfanızın kişiselleştirmelerini dışarı aktarabilir ve ardından bunları bir veya daha fazla kullanıcıya gönderebilirsiniz. Bu kullanıcıların her biri daha sonra kişiselleştirmeyi içeri aktarabilir. Kişiselleştirme araç çubuğunda, kişiselleştirmeleri dışarı ve içeri aktarmanıza olanak sağlayan düğmeler vardır.

> [!NOTE]
> Tuval uygulaması harici kullanıcılarla paylaşıldıysa, bu kullanıcılar Finans ve Operasyon uygulamalarının içindeki gömülü uygulamayı kullanamaz. Ancak, bunlar doğrudan Power Apps içinden uygulamaya erişebilir. Dış kullanıcılar, Finans ve Operasyon uygulamasının dağıtıldığı Microsoft 365 Azure Directory'e ait olmayan konukları ve kullanıcıları içerir.

Üründeki kişiselleştirme özelliklerini ve onları nasıl kullanacağınıza dair daha fazla ayrıntı için bkz. [kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Finans ve Operasyon uygulamalarından gönderilen verileri kullanan bir tuval uygulaması oluşturma

Bir Finans ve Operasyon uygulamasına gömülecek bir tuval uygulaması oluşturduğunuzda, sürecin önemli bir parçası bu Finans ve Operasyon uygulamasındaki giriş verilerini kullanmaktır. Power Apps geliştirme deneyiminden, bir Finans ve Operasyon uygulamasından geçirilen giriş verilerine **Param("EntityId")** değişkeni kullanılarak erişilebilir. Ek olarak, 10.0.19 sürümünden başlayarak, geçerli tüzel kişilik aynı zamanda **Param("cmp")** değişkeni aracılığıyla tuval uygulamasına içerik olarak geçirilir. 

Örneğin, uygulamanın OnStart işlevinde, Finans ve Operasyon uygulamalarından giriş verilerini aşağıdaki gibi bir değişkene ayarlayabilirsiniz:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Tuval uygulamasını görüntüleme

Finans ve Operasyon uygulamalarındaki bir sayfada gömülü tuval uygulamasını görüntülemek için, gömülü bir uygulamaya sahip bir sayfaya gitmeniz yeterlidir. Uygulamalara, standart Eylem Bölmesi'ndeki **Power Apps** düğmesi kullanılarak erişilebildiğini unutmayın. Alternatif olarak, bir sayfada yeni bir sekme, hızlı sekme, dikey pencere veya bir çalışma alanındaki yeni bir bölüm olarak doğrudan görüntülenebilirler. Kullanıcılar sayfaya ilk kez bir uygulama yüklemeye çalıştıklarında, oturum açmaları istenir. Bu adım, kullanıcıların uygulamayı kullanmak için uygun izinlere sahip olmasını gerektirir.

## <a name="editing-an-embedded-app"></a>Katıştırılmış bir uygulamayı düzenleme

Bir uygulama bir sayfaya katıştırıldıktan sonra, bu uygulamanın yapılandırmasında bazı değişiklikler yapmanız gerekebilir. Örneğin, katıştırılmış uygulama ile ilişkilendirilen etikette değişiklik yapmak isteyebilirsiniz veya uygulamanın yeni bir sürümü oluşturulduğunda Uygulama Kodunu en son uygulamayı gösterecek şekilde güncelleştirmeniz gerekebilir.

Katıştırılmış bir uygulama yapılandırmasını düzenlemek için şu adımları izleyin:

1. **Uygulamayı düzenle** bölmesine gidin.

    - Katıştırılmış uygulamaya Power Apps menü düğmesi aracılığıyla erişiliyorsa Power Apps menü düğmesini seçip basılı tutun (veya sağ tıklayın) ve **Kişiselleştir**'i seçin. Yapılandırmak istediğiniz uygulamayı **Uygulama seçin** açılır menüsünden seçin.
    - Katıştırılmış uygulama doğrudan sayfa üzerinde görünüyorsa **Seçenekler**'i ve ardından **Bu sayfayı kişiselleştir**'i seçin. **Seç** aracını kullanarak, katıştırılmış uygulamaya tıklayın.
    - Katıştırılmış uygulama panodan eklendiyse panoyu açın, tuval uygulamasıyla ilişkili kutucuğu seçip basılı tutun (veya sağ tıklayın), **Kişiselleştir**'i ve ardından **Sayfayı düzenle**'yi seçin.

2. Uygulama yapılandırmasında gerekli değişiklikleri yapın ve **Kaydet**'e tıklayın.

## <a name="removing-an-app"></a>Uygulamayı kaldırma

Uygulama bir sayfaya katıştırıldıktan sonra gerektiğinde kaldırmanın birkaç yolu vardır:

- Bu konunun önceki kısmında yer alan [Katıştırılmış bir uygulamayı düzenleme](#editing-an-embedded-app) bölümündeki yönergeleri kullanarak **Uygulama düzenle** bölmesine gidin. Bölmenin kaldırmak istediğiniz katıştırılmış uygulama ile ilgili bilgileri görüntülendiğini doğrulayın ve ardından **Sil** düğmesine tıklayın.
- Katıştırılmış uygulama panodan eklendiyse panoyu açın, tuval uygulamasıyla ilişkili kutucuğu seçip basılı tutun (veya sağ tıklayın), **Kişiselleştir**'i ve ardından **Sayfayı kaldır**'ı seçin. 
- Katıştırılmış uygulama, kişiselleştirme verisi olarak kaydedildiğinden, sayfanın kişiselleştirmesini temizlemek bu sayfadaki tüm katıştırılmış uygulamaları da kaldırır. Sayfanın kişiselleştirmesini temizlemek kalıcı bir işlemdir ve geri alınamaz. Bir sayfadaki kişiselleştirmelerinizi kaldırmak için **Seçenekler**'i ve ardından **Bu sayfayı kişiselleştir**'i ve son olarak **Temizle** düğmesini seçin. Tarayıcınızı yenilendikten sonra, bu sayfadaki önceki tüm özelleştirmeler kaldırılır. Kişiselleştirme kullanarak sayfaları en iyi duruma getirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

## <a name="appendix"></a>Ek

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Geliştirici] Form üzerinde bir tuval uygulaması modelleme

Bu konu kişiselleştirme üzerinden tuval uygulamalara odaklanırken, geliştiricilerin Visual Studio geliştirme deneyimini kullanarak formlara tuval uygulama ekleme seçeneği de vardır. Bunu yapmak için forma bir PowerAppsHostControl eklemeniz yeterlidir. Denetimdeki mevcut meta veri özellikleri, kişiselleştirme deneyimle aynı özelliklere sahiptir.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Geliştirici tarafından] Uygulamanın katıştırıldığı yeri belirtme

Varsayılan olarak kullanıcılar, Power Apps menü düğmesi altından veya doğrudan sayfaya bir sekme, hızlı sekme, dikey pencere veya çalışma alanına yeni bir bölüm olarak herhangi bir sayfaya uygulamalar katıştırabilir. Ancak, gerekirse geliştiriciler aşağıdaki yöntemleri kullanarak bu özelliği yalnızca uygulamaların belirli sayfalara katıştırılmasına izin verecek şekilde yapılandırabilir:

- **isPowerAppPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, Power Apps menü düğmesi görüntülenmez ve kullanıcılar uygulamaları bu sayfadaki bir sekme dahil olmak üzere herhangi bir yere katıştıramaz.
- **isPowerAppTabPersonalizationEnabled** – Bu yöntem belirli bir sayfa için yanlış değeri döndürürse, kullanıcılar uygulamaları doğrudan sayfa üzerine bir sekme, hızlı sekme veya panorama bölümü olarak ekleyemez. Sayfada katıştırmaya izin verilmiş olması durumunda, kullanıcılar uygulamaları Power Apps menü düğmesiyle katıştırabilecektir.

Aşağıdaki örnek uygulamaların nereye katıştırılabileceğini yapılandırmak için gerekli olan iki yöntemi içeren yeni bir sınıfı göstermektedir.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
