---
title: Eyleme bağlı ER hedeflerini yapılandırma
description: Bu konuda, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçimi için eyleme bağlı hedeflerin nasıl yapılandırılacağı açıklanmaktadır.
author: NickSelin
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 93adc5b91667fdcd5969439994170fe7d28258fc9f5762d1262d8e72862c4f5f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762260"
---
# <a name="configure-action-dependent-er-destinations"></a>Eyleme bağlı ER hedeflerini yapılandırma

[!include [banner](../includes/banner.md)]

Giden belge oluşturmak üzere kullanılan [Elektronik raporlama (ER)](general-electronic-reporting.md) [biçimi](general-electronic-reporting.md#FormatComponentOutbound) [yapılandırmasının](general-electronic-reporting.md#Configuration) her çıkış bileşeni (klasör veya dosya) için [hedefleri](electronic-reporting-destinations.md) yapılandırabilirsiniz. Bu türde bir ER biçimi çalıştıran ve uygun erişim haklarına sahip olan kullanıcılar, yapılandırılmış hedef ayarlarını çalışma zamanında da değiştirebilir.

Microsoft Dynamics 365 Finance **10.0.17 sürümünde ve sonraki sürümlerde** bir ER biçimi, kullanıcının söz konusu ER biçimini çalıştırarak gerçekleştirdiği eylem kodunu [hazırlayarak](er-apis-app10-0-17.md) çalıştırılabilir. Örneğin, **Alacak hesapları** modülündeki Yazdırma ayönetimi ayarlarında, serbest metin faturası gibi belirli iş belgelerini oluşturan bir ER biçimi seçebilirsiniz. Daha sonra, faturanın önizlemesini görmek için **Görüntüle**'yi veya faturayı yazıcıya göndermek için **Yazdır**'ı seçebilirsiniz. Çalışma zamanında çalışan ER biçimi için bir kullanıcı eylemi geçirilirse farklı kullanıcı eylemleri için farklı ER hedefleri yapılandırabilirsiniz. Bu konuda, bu ER biçimi türü için ER hedeflerinin nasıl yapılandırılacağı açıklanmaktadır.

## <a name="make-action-dependent-er-destinations-available"></a>Eyleme bağlı ER hedeflerini kullanılabilir hale getirme

Geçerli Finance kurulumunda eyleme bağlı ER hedeflerini yapılandırmak ve [yeni](er-apis-app10-0-17.md) ER API'sini etkinleştirmek için [Özellik yönetimi](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) çalışma alanını açın ve **Farklı PM eylemleri için kullanılacak belirli ER hedeflerini yapılandır** özelliğini etkinleştirin. Çalışma zamanında [belirli](#reports-list-wave1) raporlar için yapılandırılan ER hedeflerini kullanmak için **Kullanıcı eylemine özgü ER hedeflerine bağlı PM raporlarının çıkışlarını yönlendir (1. dalga)** özelliğini etkinleştirin.

## <a name="configure-action-dependent-er-destinations"></a>Eyleme bağlı ER hedeflerini yapılandırma

**Farklı PM eylemleri için kullanılacak belirli ER hedeflerini yapılandır** özelliğini etkinleştirdiğinizde, **Elektronik raporlama hedefi** sayfasının **Dosya hedefi** hızlı sekmesinde eyleme bağlı ER hedeflerini yapılandırabilirsiniz. Her bileşen için, bir kayıt ekleyebilir ve belirli ER hedeflerini etkinleştirebilirsiniz. Her kayıt için, yapılandırılmış ER hedeflerinin geçerli olacağı belge türünü belirtmeniz gerekir. **Belge türü** alanında, aşağıdaki değerlerden birini seçin:

- Çalışma zamanında herhangi bir kullanıcı eylemi kodu sağlanmazsa yapılandırılan hedeflerin uygulanması için **Elektronik**'i seçin.
- Çalışma zamanında herhangi bir kullanıcı eylemi kodu sağlanmazsa yapılandırılan hedeflerin uygulanması için **Yazdırma yönetimi**'ni seçin.
- Çalışma zamanında herhangi bir kullanıcı eyleminin sağlanıp sağlanmamasına bakılmaksızın, her zaman yapılandırılan hedeflerin uygulanması için **Her** seçeneğini belirleyin.

**Yazdırma yönetimi** belge türünü seçerseniz, yapılandırılmış ER hedeflerin uygulanacağı kullanıcı eylemlerini belirtmeniz gerekir. **Yazdırma yönetimi eylemi** alanında, aşağıdaki değerlerden birini seçin:

- Çalışma zamanında **Görüntüle** kullanıcı eylemi sağlanırsa yapılandırılan hedeflerin uygulanması için **Görüntüle**'yi seçin.
- Çalışma zamanında **Yazdır** kullanıcı eylemi sağlanırsa yapılandırılan hedeflerin uygulanması için **Yazdır**'ı seçin.
- Çalışma zamanında **Gönder** kullanıcı eylemi sağlanırsa yapılandırılan hedeflerin uygulanması için **Gönder**'i seçin.

> [!NOTE]
> Tek bir hedef kaydı için birden fazla eylem seçilebilir.

**Her** belge türünü seçerseniz **Yazdırma yönetimi eylemi** alanında kullanıcı eylemi olarak **Otomatik Algıla** otomatik olarak seçilir ve aşağıdaki davranış gerçekleşir:

- Çalışma zamanında herhangi bir kullanıcı eylemi kodu sağlanmazsa yapılandırılan tüm ER hedefleri uygulanır.
- Çalışma zamanında bir kullanıcı eylemi kodu sağlanırsa, belirli bir eylem için önceden tanımlanmış **etkinleştirilmiş olup olmamasına bakılmaksızın** ER hedefi uygulanır.

    - Çalışma zamanında **Görüntüle** eylemi sağlanırsa **Ekran** ER hedefi uygulanır.
    - Çalışma zamanında **Gönder** eylemi sağlanırsa **E-posta** ER hedefi uygulanır.
    - Çalışma zamanında **Yazdır** eylemi sağlanırsa **Yazıcı** ER hedefi uygulanır.

Örneğin, deftere naklettiğinizde [serbest metin faturasını](../../../finance/accounts-receivable/create-free-text-invoice-new.md) yazdırmak için **Serbest metin faturası (Excel)** ER biçimini kullanabilirsiniz. Oluşturulan bir belgeyi yönlendirmek için bu ER biçimi için ER hedeflerini yapılandırmalısınız. Örneğin, bu ER hedeflerini, oluşturulan bir belgede aşağıdakileri gerçekleştirecek şekilde yapılandırmanız gerekebilir:

- ER biçimi çalıştırılmasına rağmen eylem kodu sağlanmazsa belgeyi arşivleyin (ör. belgenin elektronik olarak gönderilmesi durumunda).
- Kullanıcı **Görüntüle** eylemini gerçekleştirdiğinde belgeyi web tarayıcısında önizlemeyle görüntüleyin.
- Kullanıcı **Yazdır** eylemini gerçekleştirdiğinde belgeyi arşivleyin ve yazdırın.
- Kullanıcı **Gönder** eylemini gerçekleştirdiğinde belgeyi arşivleyin ve giden e-posta iletisinin eki olarak e-postayla gönderin.

Aşağıdaki çizimde, tek bir kullanıcı eylemi için her kayıt yapılandırma işleminde ER hedeflerini ayrı hedef kayıtları kümesi olarak nasıl yapılandırabileceğiniz gösterilmektedir.

![Tek bir kullanıcı eylemi için her hedef kaydı yapılandırıldığında ER biçimi için eyleme bağlı hedef ayarları olan elektronik raporlama hedefi sayfası.](./media/er-destination-action-dependent-01.png)

Aşağıdaki çizimde, tek bir hedef için her kayıt yapılandırma işleminde ER hedeflerini ayrı hedef kayıtları kümesi olarak yapılandırmayı alternatif olarak nasıl yapabileceğiniz gösterilmektedir.

![Tek bir hedef için her hedef kaydı yapılandırıldığında ER biçimi için eyleme bağlı hedef ayarları olan elektronik raporlama hedefi sayfası.](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Çalışan ER biçimi için bir eylem kodu sağlanıp söz konusu eylem kodu için hiçbir hedef yapılandırılmamışsa [varsayılan](electronic-reporting-destinations.md#default-behavior) hedef davranışı uygulanır.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Çalışma zamanında eyleme bağlı ER hedeflerini değiştirme

Bir ER biçimi çalıştırıldığında, çalışma zamanında yapılandırılan hedef ayarlarını değiştirmek için uygun [izinlere](electronic-reporting-destinations.md#security-considerations) sahip kullanıcılar tarafından kullanıcı eylemleri sağlanırsa, yapılandırılan hedef ayarlarını değiştirme seçeneği sunan bir iletişim kutusu gösterilir. Bu iletişim kutusu isteğe bağlıdır ve görünümü, ER çerçevesinin ER biçimini çalıştırmak için yaptığı çağrının nasıl uygulandığına bağlıdır. Bu iletişim kutusu görüntülenirse içindeki ER hedefleri sağlanan kullanıcı eylemine göre etkinleştirilir.

Aşağıdaki çizimde, serbest metin faturası [deftere nakledildiğinde](../../../finance/accounts-receivable/create-free-text-invoice-new.md) görüntülenen **Elektronik raporlama biçimi hedefleri** iletişim kutusunun bir örneği gösterilir. **Yazıcı** eylemi sağlanmışsa ve bu konunun önceki kısımlarında belirtilen şekilde bu biçim için ER hedefleri yapılandırılmışsa bu belgeyi oluşturmak için **Serbest metin faturası (Excel)** ER biçimi çalıştırılır.

![Çalıştırılan ER biçimi için başlangıçta yapılandırılmış ER hedeflerini değiştirme seçeneği sunan iletişim kutusu.](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Çalıştırılan ER biçiminin birkaç bileşeni için ER hedefi yapılandırdıysanız ER biçiminin yapılandırılmış her bileşeni için ayrı olarak bir seçenek sunulur.

## <a name="verify-the-provided-user-action"></a>Sağlanan kullanıcı eylemini doğrula

Belirli bir kullanıcı eylemi gerçekleştirirken çalıştırılan ER biçimi için hangi kullanıcı eyleminin sağlandığını (sağlanmışsa) doğrulayabilirsiniz. Eyleme bağlı ER hedeflerinini yapılandırmanız gereken ancak hangi kullanıcı eylemi kodunun sağlandığından (sağlanmışsa) emin olmadığınız durumlarda bu doğrulama önemlidir. Örneğin, serbest metin faturasını deftere nakletmeye başlayıp **Serbest metin faturasını deftere naklet** iletişim kutusundaki **Faturayı yazdır** seçeneğini **Evet** olarak ayarladığınızda **Yazdırma yönetimi hedefini kullan** seçeneğini **Evet** veya **Hayır** olarak ayarlayın.

Sağlanan kullanıcı eylem kodunu doğrulamak için bu adımları izleyin.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Hata ayıklama modu** seçeneğini **Evet** olarak [ayarlayın](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature).
4. ER biçimini çalıştırarak kullanıcı eylemini gerçekleştirin. ER kullanıcı parametrelerinin şirkete özgü ve kullanıcıya özgü olduğunu unutmayın.
5. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar hata ayıklama**'ya gidin.
6. **Yapılandırma hata ayıklama günlükleri** sayfasında, ER biçimi çalıştırmanızın günlüğünü bulmak için ER çalıştırma günlüklerini filtreleyin.
7. ER biçimi çalıştırması için sağlanan bir eylem varsa sağlanan kullanıcı eylemi kodunu gösteren kaydı içermesi gereken günlük girişlerini inceleyin.

    ![ER biçiminin filtreli çalıştırılması için sağlanan kullanıcı eylemi kodu hakkında bilgiler içeren elektronik raporlama çalıştırma günlükleri sayfası.](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">İş belgelerinin listesi (1. dalga)</a>

Aşağıdaki iş belgeleri listesi, **Kullanıcı eylemine özgü ER hedeflerine bağlı PM raporlarının çıkışlarını yönlendir (1. dalga)** özelliği tarafından denetlenir:

- Müşteri faturası (Serbest metin faturası)
- Müşteri faturası (Satış faturası)
- Satın alma siparişi
- Satınalma siparişi satınalma sorgusu
- Satış siparişi onayı
- Tahsilatlar mektubu dekontu
- Müşteri hesap ekstresi
- Vade farkı dekontu
- Satıcı ödeme ihbarı
- Teklif talebi

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)

[Application update 10.0.17 için elektronik raporlama çerçevesi API değişiklikleri](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]