---
title: Lifecycle Services'e bir yapılandırma yükleme
description: Bu konuda, yeni bir Elektronik raporlama (ER) yapılandırması oluşturma ve bunu Microsoft Dynamics Lifecycle Services'a (LCS) yükleme açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092553"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Lifecycle Services'e bir yapılandırma yükleme

[!include [banner](../../includes/banner.md)]

Aşağıdaki konuda, Sistem yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının yeni bir [Elektronik Raporlama (ER) yapılandırması](../general-electronic-reporting.md#Configuration) oluşturarak Microsoft Dynamics Lifecycle Services (LCS)'de [proje düzeyi Varlık kitaplığı'na](../../lifecycle-services/asset-library.md) yüklemesi açıklanmaktadır.

Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacak ve bunu LCS'ye yükleyeceksiniz. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette tamamlanabilir. Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) adımlarını tamamlamanız gerekir. LCS'ye erişim de gereklidir.

1. Aşağıdaki rollerden birini kullanarak uygulamada oturum açın:

    - Elektronik raporlama geliştirici
    - Sistem yöneticisi

2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Litware, Inc.** öğesini seçin ve **Etkin** olarak ayarlayın.
4. **Yapılandırmalar**'ı seçin.

<a name="accessconditions"></a>
> [!NOTE]
> Geçerli Dynamics 365 Finance kullanıcısının, ER konfigürasyonlarını içe aktarmak için kullanılacak [Varlık kitaplığı'nı](../../lifecycle-services/asset-library.md#asset-library-support) içeren LCS projesine üye olduğundan emin olun.
>
> Bir LCS projesine Finance içinde kullanılan etki alanından farklı bir etki alanını temsil eden bir ER havuzundan erişemezsiniz. Denediğinizde, boş bir LCS proje listesi görüntülenir ve bu yapılandırmaları LCS'de proje düzeyi Varlık kitaplığı'ndan içe aktarmanız mümkün olmayacaktır. ER yapılandırmalarını içe aktarmak için kullanılan bir ER havuzundan proje düzeyi Varlık kitaplıkları'na erişmek için, geçerli Finance örneğinin sağlandığı kiracıya (etki alanı) ait bir kullanıcının kimlik bilgilerini kullanarak Finance uygulamasında oturum açın.

## <a name="create-a-new-data-model-configuration"></a>Yeni bir veri modeli yapılandırması oluşturun

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. Açılır iletişim kutusunu açmak için **Yapılandırmalar** sayfasında **Yapılandırma oluştur**'u seçin.

    Bu örnekte elektronik belgeler için örnek bir veri modeli içeren bir yapılandırma oluşturacaksınız. Bu veri modeli yapılandırması daha sonra LCS'ye yüklenecektir.

3. **Ad** alanına **Örnek model yapılandırması** değerini girin.
4. **Açıklama** alanına **Örnek model yapılandırması** değerini girin.
5. **Yapılandırma oluştur**'u seçin.
6. **Model Tasarımcısı**'nı seçin.
7. **Yeni**'yi seçin.
8. **Ad** alanına **Giriş noktası** değerini girin.
9. **Ekle**'yi seçin.
10. **Kaydet**'i seçin.
11. Sayfayı kapatın.
12. **Durumu değiştir**'i seçin.
13. **Tamamlandı**'yı seçin.
14. **Tamam**'ı seçin.
15. Sayfayı kapatın.

## <a name="register-a-new-repository"></a>Yeni bir depo kaydetme

1. **Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.

2. **Yapılandırma sağlayıcıları** bölümünde, **Liteware, Inc.** kutucuğunu seçin.

3. **Liteware, Inc.** kutucuğunda, **Depolar**'a tıklayın.

    Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.

4. Açılır iletişim kutusunu açmak için **Ekle**'yi seçin.

    Şimdi yeni bir depo ekleyebilirsiniz.

5. **Yapılandırma deposu giriş** alanında **LCS**'yi seçin.
6. **Depo oluştur**'u seçin.
7. **Proje** alanına bir değer girin veya seçin.

    Bu örnekte, istenilen LCS projesini seçin. Projeye [erişiminiz](#accessconditions) olmalıdır.

8. **Tamam**'ı seçin.

    Yeni bir havuz girişini tamamlayın.

9. Listede, seçili satırı işaretleyin.

    Bu örnekte, **LCS** depo kaydını seçin.

    Kayıtlı bir deponun geçerli sağlayıcı tarafından işaretlendiğini unutmayın. Başka bir deyişle, yalnızca bu sağlayıcıya ait olan yapılandırmalar bu depoda yer alabilir ve bu nedenle seçili LCS projesine yüklenebilir.

10. **Aç**'ı seçin.

    ER yapılandırmalarının listesini görüntülemek için havuzu açarsınız. Seçili proje ER yapılandırmaları paylaşımı için henüz kullanılmamışsa, liste boş olur.

11. Sayfayı kapatın.
12. Sayfayı kapatın.

## <a name="upload-a-configuration-into-lcs"></a>Bir yapılandırmayı LCS'ye yükleme

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Örnek model yapılandırması** seçeneğini belirleyin.

    Tamamlanmış olan oluşturulmuş bir yapılandırmayı seçmeniz gerekir.

3. Listede, istenen kaydı bulun ve seçin.

    Bu örnek için seçili yapılandırmanın **Tamamlandı** durumda olan sürümünü seçin.

4. **Durumu değiştir**'i seçin.
5. **Paylaş**'ı seçin.

    Yapılandırma LCS 'de yayımlandığında yapılandırmanın durumu, **Tamamlandı**'dan **Paylaşıldı**'ya geçer.

6. **Tamam**'ı seçin.
7. Listede, istenen kaydı bulun ve seçin.

    Bu örnek için yapılandırmanın **Paylaşıldı** durumda olan sürümünü seçin.

    Seçili sürümün durumunun **Tamamlandı**'dan **Paylaşıldı**'ya geçtiğini unutmayın.

8. Sayfayı kapatın.
9. **Depolar**'ı seçin.

    Artık Litware, Inc. yapılandırma sağlayıcısı için depoların listesini açabilirsiniz.

10. **Aç**'ı seçin.

    Bu örnekte, **LCS** deposunu seçin ve açın.

    Seçili yapılandırmanın seçili LCS projesinin bir varlığı olarak gösterildiğini unutmayın.

11. <https://lcs.dynamics.com> adresine giderek LCS'yi açın.
12. Depo kaydı için daha önce kullanılan bir projeyi açın.
13. Projenin Varlık kitaplığı'nı açın.
14. **GER yapılandırması** varlık türünü seçin.

    Karşıya yüklediğiniz ER yapılandırması listelenmelidir.

    Bu LCS projesine sağlayıcıların erişimi varsa, karşıya yüklenen LCS yapılandırmasının başka bir örneğe aktarılabildiğini unutmayın.
