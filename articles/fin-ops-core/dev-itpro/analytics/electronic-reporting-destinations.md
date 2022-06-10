---
title: Elektronik raporlama (ER) hedefleri
description: Bu konuda, elektronik raporlama hedeflerinin yönetimi, desteklenen hedef türleri ve güvenlik konuları hakkında bilgi verilmektedir.
author: nselin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e3154cb62531bf956365b420b454c98ead7f7335
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780474"
---
# <a name="electronic-reporting-er-destinations"></a>Elektronik raporlama (ER) hedefleri

[!include [banner](../includes/banner.md)]

Her bir Elektronik raporlama (ER) biçimi yapılandırması ve bunun çıkış bileşeni (bir klasör veya bir dosya) için bir hedef yapılandırabilirsiniz. Uygun erişim haklarına sahip kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir. Bu konu, ER hedef yönetimini, desteklenen hedeflerin türlerini ve güvenlik konularını açıklamaktadır.

ER biçim yapılandırmaları genellikle en az bir çıkış bileşeni içerir: dosya. Genelde yapılandırmalar tek veya birden fazla klasörde gruplanan farklı türlerde birden fazla dosya çıkış bileşeni içerir (örneğin, XML, TXT, XLSX, DOCX, PDF). ER hedef yönetimi her bir bileşen çalıştırıldığında ne olduğunu önceden yapılandırmanızı sağlar. Bir yapılandırma çalıştırıldığında, varsayılan olarak, bir dosyayı açmanıza veya kaydetmenize olanak sağlayan bir iletişim kutusu gösterilir. Aynı çalışma davranışı bir ER yapılandırmasını içe aktardığınızda ve bunun için belli bir hedef yapılandırmadığınızda da oluşur. Ana çıkış bileşeni için bir hedef oluşturulduktan sonra bu hedef varsayılan davranışı geçersiz kılar ve klasör veya dosya hedef ayarlarına göre gönderilir.

## <a name="availability-and-general-prerequisites"></a>Kullanılabilirlik ve genel önkoşulları

ER hedeflerinin işlevselliği Microsoft Dynamics AX 7.0 (Şubat 2016) sürümünde kullanılamaz. Bu nedenle, aşağıdaki hedef türlerini kullanmak için Microsoft Dynamics 365 for Operations 1611 (Kasım 2016) veya daha ileri sürümü yüklemelisiniz.

- [E-posta](er-destination-type-email.md)
- [Arşivle](er-destination-type-archive.md)
- [Dosya](er-destination-type-file.md)
- [Ekran](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Alternatif olarak, aşağıdaki önkoşullardan birini de yükleyebilirsiniz. Ancak, bu alternatiflerin daha sınırlı bir ER hedef deneyimi sağladığını unutmayın.

- Microsoft Dynamics AX uygulama sürümü 7.0.1 (Mayıs 2016)
- [Elektronik raporlama hedef yönetim uygulaması düzeltmesi](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Aynı zamanda bir [Yazdırma](er-destination-type-print.md) hedefi türü vardır. Bunu kullanmak için Microsoft Microsoft Dynamics 365 Finance 10.0.9 (2020 Nisan) sürümünü yüklemelisiniz.

## <a name="overview"></a>Genel Bakış

Yalnızca, geçerli Finance kurulumuna [aktarılmış](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) ER yapılandırmaları ve **Elektronik raporlama yapılandırmaları** sayfasında kullanılabilen biçimler için hedefler ayarlayabilirsiniz. ER hedef yönetimi işlevselliği, **Organizasyon yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama hedefi**'nde kullanılabilir.

### <a name="default-behavior"></a>Varsayılan davranış

Bir ER biçimi yapılandırmasının varsayılan davranışı, ER biçimi başladığında belirttiğiniz yürütme türüne bağlıdır.

**Intrastat Raporu** iletişim kutusunda, **Arka planda çalıştır** hızlı sekmesinde **Toplu işleme** seçeneğini **Hayır** olarak ayarlasanız bir ER biçimi hemen etkileşimli modda çalıştırılır. Bu yürütme başarılı şekilde tamamlandığında, oluşturulan bir giden belge indirmek üzere kullanılabilir duruma getirilir.

**Toplu işleme** seçeneğini **Evet** olarak ayarlarsanız, ER biçimi [toplu iş](../sysadmin/batch-processing-overview.md) modunda çalıştırılır. Uygun toplu iş **ER parametreleri** iletişim kutusunun **Arka planda çalıştır** sekmesinde belirttiğiniz parametrelere göre oluşturulur.

> [!NOTE]
> İş açıklaması, bir ER biçimi eşlemesinin çalışması hakkında bilgi verir. Ayrıca çalıştırılan ER bileşeninin adını da içerir:

[![ER biçimi çalıştırma.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Bu işle ilgili bilgileri birkaç yerde bulabilirsiniz:

- Planlanan işin durumunu kontrol etmek için **Ortak** \> **Sorgular** \> **Toplu işler** \> **Toplu işlerim**'e gidin.
- Planlanan işin durumunu ve tamamlanan işin yürütme sonuçlarını kontrol etmek için **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama işleri**'ne gidin. İş yürütme başarıyla tamamlandığında, oluşturulan çıktı belgesini almak için **Elektronik raporlama işleri** sayfasında **Dosyaları göster**'i seçin.

    > [!NOTE]
    > Bu belge geçerli iş kaydının eki olarak depolanır ve [Belge yönetimi](../../fin-ops/organization-administration/configure-document-management.md) çerçevesi tarafından denetlenir. Bu türdeki ER yapılarını depolamak için kullanılan [belge türü](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) [ER parametrelerinde](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) yapılandırılır.

- İş yürütme sırasında oluşturulan hataların ve uyarıların listesini görmek için **Elektronik raporlama işleri** sayfasında, **Dosyaları göster**'i seçin.

    [![ER işleri listesini gözden geçirme.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Kullanıcı tarafından yapılandırılan davranış

**Elektronik raporlama hedefi** sayfasında, bir yapılandırma için varsayılan davranışı geçersiz kılabilirsiniz. Siz **Yeni** ve ardından **Referans** alanını seçene kadar içe aktarılan yapılandırmalar bu sayfada gösterilmez, hedef ayarlarını oluşturmak için bir yapılandırma seçin.

[![Referans alanında bir yapılandırma seçme.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Referans oluşturduktan sonra, başvurulan ER biçiminin her bir **Klasör** veya **Dosya** çıktı bileşeni için bir dosya hedefi oluşturabilirsiniz.

[![Bir dosya hedefi oluşturma.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Bunun ardından, **Hedef ayarları** iletişim kutusunda dosya için tekil hedefleri etkinleştirebilir ve devre dışı bırakabilirsiniz. **Ayarlar** düğmesi seçili dosya hedefi için tüm hedefleri denetlemek amacıyla kullanılır. **Hedef ayarları** iletişim kutusunda **Etkin** seçeneğini ayarlayarak her hedefi ayrı olarak denetleyebilirsiniz.

**Sürüm 10.0.9 sürümünden önceki** Finance sürümlerinde, **Dosya Adı** alanında seçilen, klasör veya dosya gibi, aynı biçimdeki her bir çıkış bileşeni için **bir dosya hedefi** oluşturabilirsiniz. Ancak, **sürüm 10.0.9 ve sonrasında**, aynı biçimdeki her bir çıktı bileşeni için **birden çok dosya hedefi** oluşturabilirsiniz.

Örneğin, Excel biçiminde bir giden belge oluşturmak için kullanılan bir dosya bileşeni için dosya hedeflerini yapılandırmak amacıyla bu özelliği kullanabilirsiniz. Bir hedef ([Arşiv](er-destination-type-archive.md)), özgün Excel dosyasını ER işleri arşivinde depolayacak şekilde ve bir başka hedef de ([E-posta](er-destination-type-email.md)) aynı anda Excel dosyasını PDF biçimine [dönüştürecek](#OutputConversionToPDF) ve PDF dosyasını e-postayla gönderecek şekilde yapılandırılabilir.

[![Tek bir biçim öğesi için birden çok hedef yapılandırma.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Bir ER biçimi çalıştırdığınızda, biçim bileşenleri için yapılandırılan tüm hedefler her zaman çalıştırılır. Ayrıca, Finance **10.0.17 sürümünde ve sonraki sürümlerde**, ER hedefleri işlevi iyileştirilmiştir ve tek bir ER biçimi için farklı hedef kümelerini yapılandırmanıza izin verir. Bu yapılandırma, her kümeyi belirli bir kullanıcı eylemine göre yapılandırılmış olarak işaretler. Kullanıcının ER biçimini çalıştırarak gerçekleştirdiği eylemin sağlanabilmesi için ER API'si [uzatılmıştır](er-apis-app10-0-17.md). Sağlanan eylem kodu, ER hedeflerine geçirilir. Sağlanan eylem koduna bağlı olarak ER biçiminin farklı hedeflerini çalıştırabilirsiniz. Daha fazla bilgi için bkz. [Eyleme bağlı ER hedeflerini yapılandırma](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Hedef türleri

ER biçimleri için şu anda aşağıdaki hedefler desteklenmektedir. Tüm türleri aynı anda devre dışı bırakabilir veya etkinleştirebilirsiniz. Bu şekilde hiçbir işlem yapmayabilir veya bileşeni tüm yapılandırılmış hedeflere gönderebilirsiniz.

- [E-posta](er-destination-type-email.md)
- [Arşivle](er-destination-type-archive.md)
- [Dosya](er-destination-type-file.md)
- [Ekran](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Yazdır](er-destination-type-print.md)

## <a name="applicability"></a>Uygulanabilirlik

Yalnızca içe aktarılan ER yapılandırmaları ve **Elektronik raporlama yapılandırmaları** sayfasında kullanılabilen biçimler için hedefleri ayarlayabilirsiniz.

> [!NOTE]
> Yapılandırılan hedefler şirkete özgüdür. Bir ER biçimini geçerli Finance kurulumunun farklı şirketlerinde kullanmayı planlıyorsanız, bu şirketlerin her biri için o ER biçimine ilişkin hedefler yapılandırmanız gerekir.

Seçilen biçimin dosya hedeflerini yapılandırırken, bunları tüm biçim için yapılandırın.

[![Yapılandırma bağlantısı.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Aynı zamanda, geçerli Finance kurulumuna aktarılmış olan biçimin birden çok [sürümüne](general-electronic-reporting.md#component-versioning) sahip olabilirsiniz. **Referans** alanını seçerken sunulan **Yapılandırma** bağlantısını seçerseniz bunları görüntüleyebilirsiniz.

[![Yapılandırma sürümleri.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Varsayılan olarak, yapılandırılan hedefler yalnızca **Tamamlandı** veya **Paylaşıldı** durumundaki bir ER biçimi sürümü çalıştırdığınız zaman uygulanır. Ancak, bazen bir ER biçiminin taslak sürümü çalıştırıldığında, yapılandırılmış hedefleri kullanmanız gerekir. Örneğin, biçiminizin bir taslak sürümünü değiştirirsiniz ve oluşturulan çıktının nasıl teslim edileceğini test etmek için, yapılandırılan hedefleri kullanmak isteyebilirsiniz. Taslak sürüm çalıştırıldığında bir ER biçimine yönelik hedefleri uygulamak için bu adımları izleyin.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Taslak durumu için hedefleri kullan** seçeneğini **Evet** olarak ayarlayın.

[![Taslak durumu için hedefleri kullan seçeneği.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

ER biçiminin taslak sürümünü kullanmak için, ER biçimini buna uygun olarak işaretlemeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Ayarı çalıştır** seçeneğini **Evet** olarak ayarlayın.

[![Ayarı çalıştır seçeneği.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Siz bu kurulumu tamamlandıktan sonra, **Taslağı çalıştır** seçeneği, değiştirdiğiniz ER biçimleri için kullanılabilir hale gelir. Biçim çalıştırıldığında, biçimin taslak sürümünü kullanmaya başlamak için bu seçeneği **Evet** olarak ayarlayın.

[![Taslağı çalıştır seçeneği.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Hedef başarısızlığı işleme

Genellikle, bir ER biçimi, belirli bir iş süreci kapsamında çalıştırılır. Ancak, bir ER biçiminin yürütülmesi sırasında oluşturulan bir giden belgenin teslimi bazen iş sürecinin bir parçası olmak zorundadır. Bu durumda, bir giden belgenin yapılandırılmış bir hedefe teslimi başarısız olursa, iş sürecinin yürütülmesi iptal edilmelidir. İlgili ER hedefini yapılandırmak için **Hata durumunda işlemeyi durdur** seçeneğini belirleyin.

Diyelim ki satıcı ödeme işlemini, **ISO20022 Alacak Transferi** ER biçimi çalıştırılıp ödeme dosyası ve ek belgeler (örneğin kapak sayfası ve kontrol raporu) oluşturulacak şekilde yapılandırıyorsunuz. Bir ödeme ancak kapak sayfası e-posta yoluyla başarılı bir şekilde teslim edilirse başarıyla işlenmiş kabul edilecekse, aşağıdaki çizimde gösterildiği gibi, ilgili dosya hedefindeki **CoveringLetter** bileşeni için **Hata durumunda işlemeyi durdur** onay kutusunu seçmeniz gerekir. Bu durumda, işlem için seçilen ödemenin durumu, yalnızca, oluşturulan kapak sayfasının e-postayla teslimi, Finance kurulumunda yapılandırılmış e-posta sağlayıcısı tarafından başarıyla kabul edildiği zaman **Hiçbiri**'nden **Gönderildi**'ye değişecektir.

[![Dosya hedefi hatası için işlem işlemeyi yapılandırma.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Hedefteki **CoveringLetter** bileşeni için **Hata durumunda işlemeyi durdur** onay kutusunun işaretini kaldırırsanız, kapak sayfası e-postayla başarılı bir şekilde teslim edilmese bile ödemenin başarıyla işlendiği kabul edilecektir. Örneğin, alıcının veya gönderenin e-posta adresi eksik veya yanlış olduğu için kapak yazısı gönderilemese bile, **Hiçbiri** olan ödeme durumu **Gönderildi** olarak değiştirilir.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Çıktıyı PDF'e dönüştürme

Microsoft Office (Excel veya Word) biçimindeki çıktıyı PDF biçimine dönüştürmek için PDF dönüştürme seçeneğini kullanabilirsiniz.

### <a name="make-pdf-conversion-available"></a>PDF dönüştürmeyi kullanılabilir hale getirme

PDF dönüştürme seçeneğinin geçerli Finance kurulumunda kullanılabilmesini sağlamak için **Özellik yönetimi** çalışma alanını açın ve **Elektronik raporlama giden belgelerini Microsoft Office biçimlerinden PDF'e dönüştür** özelliğini etkinleştirin.

[![Özellik yönetiminde giden belgeler için PDF dönüştürme özelliğini açma.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Uygulanabilirlik

**10.0.18 sürümünden önceki** Finance sürümlerinde PDF dönüştürme seçeneği yalnızca Office (Excel veya Word) biçiminde çıktı oluşturmak için kullanılan **Excel\\Dosya** bileşenleri için etkinleştirilebilir. Bu seçenek etkinleştirildiğinde, Office biçiminde oluşturulan çıktı otomatik olarak PDF biçimine dönüştürülür. Ancak, **Sürüm 10.0.18 ve sonrasında** Bu seçeneği **ortak\\dosya** türü bileşenleri için de etkinleştirebilirsiniz.

> [!NOTE]
> **Ortak\\ dosya** türünün ER bileşeni için PDF dönüştürme seçeneğini etkinleştirdiğinizde aldığınız uyarı iletisine dikkat edin. Bu ileti, tasarım zamanında, seçili dosya bileşeninin çalışma zamanında PDF biçimindeki içeriği veya PDF'e dönüştürülebilir içeriği göstereceğini garanti etmenin bir yolu olmadığını bildirir. Bu nedenle, yalnızca seçilen dosya bileşeninin PDF biçimindeki içeriği veya PDF'e dönüştürülebilir içeriği çalışma zamanında göstermek üzere yapılandırılmış olduğundan eminseniz bu seçeneği etkinleştirmelisiniz.
> 
> Biçim bileşeni için PDF dönüştürme seçeneğini etkinleştirirseniz bu bileşen içeriği PDF dışındaki bir formatta gösterirse ve oluşturulan içerik PDF formatına dönüştürülemiyorsa, çalışma zamanında bir özel durum oluşur. Aldığınız ileti, oluşturulan içeriğin PDF biçimine dönüştürülemediğini size bildirir.

### <a name="limitations"></a>Sınırlamalar

Finance **10.0.9 sürümü** itibarıyla, PDF dönüştürme seçeneği yalnızca bulut dağıtımları için kullanılabilir. Finance **10.0.27** sürümü itibarıyla, PDF dönüştürme seçeneği [İnternet bağlantısı](../user-interface/client-disconnected.md) etkin olan tüm şirket içi dağıtımlarda kullanılabilir.

Üretilen PDF belgesi, en fazla 300 sayfa uzunluğunda olabilir.

Finance **10.0.9 sürümü** itibarıyla, Excel çıktısından üretilen PDF belgesinde şu anda yalnızca yatay sayfa yönü desteklenmektedir. Finance **10.0.10 sürümünden** başlayarak, ER hedefi yapılandırırken Excel çıktısından oluşturulan PDF belgesindeki [sayfa yönünü belirtebilirsiniz](#SelectPdfPageOrientation).

Katıştırılmış yazı tipi içermeyen bir çıktıyı dönüştürmek için yalnızca Windows işletim sisteminin ortak sistem yazı tipleri kullanılır.

### <a name="use-the-pdf-conversion-option"></a>PDF dönüştürme seçeneğini kullanma

PDF dönüştürmeyi bir dosya hedefi için açmak için **PDF'e dönüştür** onay kutusunu seçin.

[![PDF dönüştürmeyi bir dosya hedefi için açma.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">PDF dönüştürmesi için bir sayfa yönlendirmesi seçin</a>

Excel biçiminde bir ER yapılandırması oluşturur ve bunu PDF formatına dönüştürmek istiyorsanız, PDF belgesinin sayfa yönünü açıkça belirleyebilirsiniz. Excel biçiminde bir çıktı dosyası üreten bir dosya hedefi için PDF dönüştürmesini açmak üzere **PDF 'ye Dönüştür** onay kutusunu seçtiğinizde, **sayfa yönlendirme** alanı **PDF dönüştürme ayarları** hızlı sekmesinde kullanılabilir. **Sayfa yönlendirme** alanında, tercih edilen yönlendirmeyi seçin.

[![PDF dönüştürmesi için bir sayfa yönlendirmesi seçme.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

PDF sayfa yönlendirmesini belirleme seçeneğine sahip olmak için, Finance 10.0.10 sürümünü veya sonraki bir sürümü yükleyin. **10.0.23 sürümden önceki** Finans sürümlerinde bu seçenek aşağıdaki sayfa yönlendirme seçeneklerini sunar:

- Dikey
- Yatay

Seçili sayfa yönlendirmesi Excel biçiminde oluşturulan ve PDF biçiminde dönüştürülen tüm çıkış belgelerinin sayfalarına uygulanır.

Ancak, **sürüm 10.0.23 ve sonrasında**, sayfa yönlendirme seçenekleri listesi aşağıdaki gibi genişletilmiştir:

- Dikey
- Yatay
- Çalışma sayfasına özel

**Çalışma sayfasına özgü** seçeneğini belirlediğinizde, oluşturulan Excel çalışma kitabının her çalışma sayfası, kullanılan Excel şablonunda bu çalışma sayfası için yapılandırılmış olan sayfa yönlendirmesi kullanılarak PDF'ye dönüştürülür. Bu nedenle, dikey ve yatay sayfalar içeren son PDF belgeniz olabilir. 

Word biçimindeki bir ER yapıladırması PDF biçimine dönüştürülmüşse PDF belgesinin sayfa yönü her zaman Word belgesinden alınır.

## <a name="output-unfolding"></a>Çıktı açma

ER biçiminizin **Klasör** bileşeni için bir hedef yapılandırdığınızda, bu bileşenin çıktısının yapılandırılan hedefe nasıl teslim edildiğini belirtebilirsiniz.

### <a name="make-output-unfolding-available"></a>Çıktı açmayı kullanılabilir hale getirme

Çıktı açma seçeneğini geçerli Finans örneğinde kullanılabilir hale getirmek için **Özellik yönetimi** çalışma alanını açın ve **ER hedeflerinin klasör içeriği ayrı dosyalar özelliği olarak gönderecek şekilde yapılandırılmasına izin ver** seçeneğini açın.

### <a name="applicability"></a>Uygulanabilirlik

Çıktı açma seçeneği yalnızca **Klasör** türünün biçim bileşenleri için yapılandırılabilir. Bir **Klasör** bileşenini yapılandırmaya başladığınızda, **Genel** Hızlı Sekmesi **Elektronik raporlama hedef** sayfasında kullanılabilir hale gelir. 

### <a name="use-the-output-unfolding-option"></a>Çıktı açma seçeneğini kullanma

**Genel** Hızlı Sekmesinde, **Klasörü farklı gönder** alanında aşağıdaki değerlerden birini seçin:

- **ZIP arşivi** – Oluşturulan bir dosyayı zip dosyası olarak teslim edin.
- **Ayrı dosyalar** – Oluşturulan zip dosyasının her dosyasını tek bir dosya olarak teslim edin.

    > [!NOTE]
    > **Dosyaları ayır**'ı seçtiğinizde, oluşturulan çıktı bellekte sıkıştırılmış durumda toplanır. Bu nedenle, gerçek dosya boyutu bu sınırı aşabileceği zaman sıkıştırılmış çıktı için en büyük [dosya boyutu sınırı](er-compress-outbound-files.md) uygulanır. Oluşturulan çıktının boyutunun da oldukça büyük olmasını beklediğinizde bu değeri seçmenizi öneririz.

[![Klasör biçimi bileşeni için hedef yapılandırma.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Sınırlamalar

**Klasörü farklı gönder** alanını, iç içe geçmiş diğer **Klasör** bileşenlerini içeren bir **Klasör** bileşeninin **dosyalarını ayır** olarak ayarlarsanız, ayar iç içe geçmiş **Klasör** bileşenlerine özyinelemeli olarak uygulanmaz.

## <a name="security-considerations"></a>Güvenlik ile ilgili hususlar

ER hedefleri için iki tür ayrıcalık ve görev kullanılır. Bir kullanıcının tüzel kişilik için yapılandırılan hedefleri genel olarak koruma özelliğini bir tür denetler (yani, **Elektronik raporlama hedefleri** sayfasına erişimi denetler). Diğer tür çalışma zamanında bir uygulama kullanıcısının bir ER geliştirici veya ER işlev danışmanı tarafından yapılandırılan hedef ayarlarını geçersiz kılma yeteneğini denetler.

| Rol (AOT adı)                     | Rol adı                                  | Görev (AOT adı)                     | Görev adı                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektronik raporlama geliştirici             | ERFormatDestinationConfigure        | Elektronik raporlama biçimi hedefini yapılandır                |
| ERFunctionalConsultant              | Elektronik raporlama işlev danışmanı | ERFormatDestinationConfigure        | Elektronik raporlama biçimi hedefini yapılandır                |
| PaymAccountsPayablePaymentsClerk    | Borç hesapları ödeme memuru            | ERFormatDestinationRuntimeConfigure | Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini yapılandır |
| PaymAccountsReceivablePaymentsClerk | Alacak hesapları ödeme memuru         | ERFormatDestinationRuntimeConfigure | Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini yapılandır |

> [!NOTE]
> Önceki görevlerde iki ayrıcalık kullanılır. Bu ayrıcalıklar ilgili görevlerle aynı adlara sahiptir: **ERFormatDestinationConfigure** ve **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Sıkça sorulan sorular

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Elektronik yapılandırmaları içe aktardım ve bunları Elektronik raporlama yapılandırmaları sayfasında görüyorum. Ancak bunları neden Elektronik raporlama hedefleri sayfasında görmüyorum?

**Yeni**'yi ve ardından **Referans** alanında bir yapılandırma seçtiğinizden emin olun. **Elektronik raporlama hedefleri** sayfasında, yalnızca hedeflerin yapılandırıldığı yapılandırmalar gösterilir.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Hangi Microsoft Azure Depolama hesabı ve Azure Blob depolamanın kullanıldığını tanımlamanın bir yolu var mıdır?

Hayır. Belge yönetim sistemi için tanımlanan ve kullanılan varsayılan Microsoft Azure Blob depolama kullanılır.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Hedef ayarlarındaki Dosyanın hedefinin amacı nedir? Bu ayar ne işe yarar?

**Dosya** hedefi, etkileşimli modda ER biçimi çalıştırdığınızda web tarayıcınızın iletişim kutusunu denetlemek için kullanılır. Bu hedefi etkinleştirirseniz veya bir yapılandırma için hedef tanımlanmamışsa bir çıkış dosyası oluşturulduktan sonra web tarayıcınızda kaydetme veya açma iletişim kutusu görünür.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>E-posta gönderebileceğim bir satıcı hesabını referans gösteren bir formül örneği verebilir misiniz?

Formül ER yapılandırmasına özgüdür. Örneğin, ISO 20022 Borç Transferi yapılandırmasını kullanırsanız ilgili satıcı hesabını almak için **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** veya **model.Payments.Creditor.Identification.SourceID** 'yi kullanabilirsiniz.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Biçim yapılandırmalarımdan biri bir klasörde gruplandırılmış birden fazla dosya içeriyor (örneğin, Klasör1 Dosya1, Dosya2 ve Dosya3'ü içeriyor). Klasör1.zip klasörünün hiçbir zaman oluşmaması, Dosya1'in e-posta ile gönderilmesi, Dosya2'nin SharePoint'e gönderilmesi ve yapılandırma çalışır çalışmaz Dosya3'ü açabilmem için hedefleri nasıl ayarlarım?

Önce, biçiminizin ER yapılandırmalarında kullanılabilir olması gerekir. Bu önkoşul karşılanıyorsa, **Elektronik raporlama hedefi** sayfasını açın ve yapılandırma için yeni bir referans oluşturun. Sonra her bir çıkış bileşeni için bir adet olmak üzere dört dosya hedefinizin olması gerekir. İlk dosya hedefini oluşturun, buna **Klasör** gibi bir ad verin ve yapılandırmanızda klasörü gösteren bir dosya adı seçin. Bunun ardından **Ayarlar**'ı seçin ve tüm hedeflerin devre dışı bırakıldığından emin olun. Bu dosya hedefi için klasör oluşturulmayacaktır. Varsayılan olarak, dosyalar ve ana klasörler arasındaki hiyerarşik bağımlılıklar nedeniyle dosyalar aynı şekilde davranmayacaktır. Diğer bir deyişle, bunlar her yere gönderilemeyecektir. Bu varsayılan davranışı geçersiz kılmak için her bir dosya için bir adet olmak üzere üç dosya daha oluşturmanız gerekir. Her biri için hedef ayarlarında dosyanın gönderilmesi gereken hedefi etkinleştirmeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Eyleme bağlı ER hedeflerini yapılandırma](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
