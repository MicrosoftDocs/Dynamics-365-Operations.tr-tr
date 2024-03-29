---
title: Lifecycle Services'tan bir yapılandırmayı içe aktarma
description: Bu makalede, Microsoft Dynamics Lifecycle Services (LCS) portalından Elektronik raporlama (ER) yapılandırmasının yeni sürümünün nasıl içeri aktarılacağı açıklanmaktadır.
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290379"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Lifecycle Services'tan bir yapılandırmayı içe aktarma

[!include [banner](../../includes/banner.md)]

Aşağıdaki makalede, Sistem yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının [Elektronik Raporlama (ER) yapılandırmasına](../general-electronic-reporting.md#Configuration) ait yeni bir sürümü Microsoft Dynamics Lifecycle Services (LCS)'de [proje düzeyi Varlık kitaplığı'ndan](../../lifecycle-services/asset-library.md) içe aktarması açıklanmaktadır.

> [!IMPORTANT]
> LCS'nin, ER yapılandırmaları için saklama deposu olarak kullanılma özelliği [kullanım dışı bırakılıyor](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Daha fazla bilgi için bkz. [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolamasının kullanım dışı bırakılması](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

Bu örnekte bir ER yapılandırmasının istenilen sürümünü seçecek ve Litware, Inc. adlı örnek şirket için içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşıldığından herhangi bir şirkette tamamlanabilir. Bu adımları tamamlamak için, öncelikle [Bir yapılandırmayı Lifecycle Services'e içeri almak](er-upload-configuration-into-lifecycle-services.md) bölümündeki adımları tamamlamanız gerekir. LCS'ye erişim de gereklidir.

1. Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:

    - Elektronik raporlama geliştirici
    - Sistem yöneticisi

2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Yapılandırmalar**'ı seçin.

<a name="accessconditions"></a>
> [!NOTE]
> Geçerli Dynamics 365 Finance kullanıcısının, ER yapılandırmalarını içe aktarmak için [erişmek](../../lifecycle-services/asset-library.md#asset-library-support) istediği Varlık kitaplığı'nı içeren LCS projesine üye olduğundan emin olun.
>
> Bir LCS projesine Finance içinde kullanılan etki alanından farklı bir etki alanını temsil eden bir ER havuzundan erişemezsiniz. Denediğinizde, boş bir LCS proje listesi görüntülenir ve bu yapılandırmaları LCS'de proje düzeyi Varlık kitaplığı'ndan içe aktarmanız mümkün olmayacaktır. ER yapılandırmalarını içe aktarmak için kullanılan bir ER havuzundan proje düzeyi Varlık kitaplıkları'na erişmek için, geçerli Finance örneğinin sağlandığı kiracıya (etki alanı) ait bir kullanıcının kimlik bilgilerini kullanarak Finance uygulamasında oturum açın.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Veri modeli yapılandırmasının paylaşılan bir sürümünü silme

1. **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Örnek model yapılandırması** seçeneğini belirleyin.

    Örnek veri modeli yapılandırmasının ilk sürümünü oluşturdunuz ve [Bir yapılandırmayı Lifecycle Services'e yüklemek](er-upload-configuration-into-lifecycle-services.md) yordamındaki adımlar tamamlandığında yayımladınız. Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz. Bu makalede daha sonra LCS'den bu sürümü içe aktaracaksınız.

2. Listede, istenen kaydı bulun ve seçin.

    BU örnek için yapılandırmanın **Paylaşılan** durumda olan sürümünü seçin. Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.

3. **Durumu değiştir**'i seçin.
4. **Durdur**'u seçin.

    Seçili sürümün durumunu **Paylaşılan**'dan **Durduruldu** olarak değiştirerek, silinebilir duruma getirin.

5. **Tamam**'ı seçin.
6. Listede, istenen kaydı bulun ve seçin.

    Bu örnek için yapılandırmanın **Durduruldu** durumda olan sürümünü seçin.

7. **Sil**'i seçin.
8. **Evet**'i seçin.

    Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin artık kullanılabilir olduğunu unutmayın.

9. Sayfayı kapatın.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alma

1. **Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.

2. **Yapılandırma sağlayıcıları** bölümünde, **Liteware, Inc.** kutucuğunu seçin.

3. **Liteware, Inc.** kutucuğunda, **Depolar**'a tıklayın.

    Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.

4. **Aç**'ı seçin.

    Bu örnekte, **LCS** deposunu seçin ve açın. LCS projesine ve seçili ER deposu tarafından erişilen Varlık kitaplığı'na [erişiminizin](#accessconditions) olması gerekir.

5. Listede, seçili satırı işaretleyin.

    Bu örnek için sürüm listesinden **Örnek model yapılandırması**'nın ilk sürümünü seçin.

6. **İçe aktar**'ı seçin.
7. Seçili sürümün LCS'den içe aktarıldığını onaylamak için **Evet** öğesini seçin.

    Bilgi iletisi, seçili sürümün başarıyla içe aktarıldığını onaylar.

8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. **Yapılandırmalar**'ı seçin.
11. Ağaçtan **Örnek model yapılandırması** seçeneğini belirleyin.
12. Listede, istenen kaydı bulun ve seçin.

    BU örnek için yapılandırmanın **Paylaşılan** durumda olan sürümünü seçin.

    Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
