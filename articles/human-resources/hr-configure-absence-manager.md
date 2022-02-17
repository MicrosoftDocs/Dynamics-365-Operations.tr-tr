---
title: Devamsızlık yöneticisi rolünü yapılandırma
description: Bu konuda, çalışan izninin yönetimi için Devamsızlık yöneticisi rolünün nasıl ayarlanacağı açıklanmaktadır.
author: hasrivas
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9f1c699358c9cc8de9e975886cfb72edfb0d3f31
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065238"
---
# <a name="configure-the-absence-manager-role"></a>Devamsızlık yöneticisi rolünü yapılandırma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bazı kuruluşlarda, çalışan yöneticileri ekiplerinin iznini yönetmeyebilir. Bunun yerine, devamsızlık yöneticisi bu işlemi birden çok departman ve takımdaki ekip üyeleri için işleyebilir. Devamsızlık yöneticileri izin yönetimi için aşağıdaki özelliklere sahiptir:

- Alternatif bir hiyerarşiye göre izin süresini gözden geçirin ve onaylayın.
- Takım üyesi bakiyelerini görüntüleyin.
- Devamsızlık takvimini görüntüleyin.

## <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

1. **Sistem yönetimi** çalışma alanında **Özellik yönetimi**'ni seçin.

2. **Özellik yönetimi** sekmesinde, **İzinleri devamsızlık yöneticisi yönetsin** özelliğini etkinleştirin.

## <a name="define-a-custom-hierarchy"></a>Özel hiyerarşi tanımlama

Devamsızlık yöneticisi işlevi, yapılandırılması gereken özel bir hiyerarşi kullanır.

1. **Kuruluş yönetimi** çalışma alanında **Pozisyon hiyerarşisi türleri**'ni seçin.

2. **İzin** adlı bir pozisyon hiyerarşisi türü oluşturun.

3. **İzin ve devamsızlık** çalışma alanında, **Bağlantılar** altında **İzin ve devamsızlık parametreleri**'ni seçin.

4. **Genel** sekmesinde, **Devamsızlık hiyerarşisi** açılan listesinde, daha önce oluşturduğunuz hiyerarşi türünden **İzin**'i seçin. Bu İzin hiyerarşisi ilişkilendirmesi, devamsızlık yöneticisi işlevselliğinin kullanılacağı her tüzel kişilik için tamamlanmalıdır.

Hiyerarşi türü tanımlandıktan sonra, pozisyon hiyerarşisi raporu pozisyona atanmalıdır.

1. **Kuruluş Yönetimi** çalışma alanında **Tüm pozisyonlar**'ı seçin.

2. İzin hiyerarşisinin ekleneceği konumu seçin.

3. **İlişkiler** sekmesinde **Ekle**'yi seçin.

4. **Hiyerarşi adı** alanında **İzin**'i seçin.

5. **Raporlama yapacağı pozisyon** alanında bir pozisyon seçin. Bir pozisyon seçtikten sonra çalışan adı otomatik olarak doldurulur.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Devamsızlık yöneticisi rolünü kullanıcıya atama

İzin isteklerini onaylamalarını veya reddetmelerini sağlamak için personele Devamsızlık yöneticisi rolü atanmalıdır.

1. **Sistem yöneticisi** çalışma alanında **Bağlantılar**'ı seçin.

2. **Kullanıcılar** bölümünde, **Kullanıcılar** bağlantısını seçin.

3. Kullanıcı listesinde, Devamsızlık yöneticisi rolünün atanacağı kullanıcıyı seçin.

4. **Kullanıcının rolü** sekmesinde, **Rol ata**'ya tıklayın.

5. Listeden **Devamsızlık yöneticisi** rolünü seçin. Daha sonra **Tamam**'ı seçin.

    > [!IMPORTANT]
    > Devamsızlık yöneticisi rolünü atadığınız kullanıcıya Personel rolünün de atandığından emin olun. Aksi takdirde, çalışan, özelliği kullanamaz.

6. İzin hiyerarşisini oluşturduktan sonra şu adımları izleyerek görüntüleyebilirsiniz:

    1. **Kuruluş Yönetimi** çalışma alanında **Pozisyon hiyerarşisi**'ni seçin.
    
    2. **Hiyerarşi türü** alanında **İzin**'i seçin.

## <a name="absence-manager-workspace"></a>Devamsızlık yöneticisi çalışma alanı

**Çalışan self servisi** çalışma alanında, **İzin yönetimi** sekmesi, İzin hiyerarşisinde devamsızlık yöneticisine atanan personelle ilgili devamsızlık bilgilerini gösterir. Devamsızlık yöneticisinin kullanabildiği birkaç seçenek vardır: 
 - İzin isteklerini inceleyin.</br>
 - Bir çalışan adına izin isteği gönderin.</br>
 - İzin hiyerarşisinin parçası olarak izinlere atanan tüm çalışanları görüntüleyin.</br>
 - Devamsızlık yöneticisi takvimini görüntüleyin.</br>

**İzin yönetimi** çalışma alanında iki sekme vardır:
 - **İzin istekleri**: Bu sekme, devamsızlık yöneticisinin onaylayabildiği tüm bekleyen izin isteklerini listeler. Devamsızlık yöneticisi aynı anda birden fazla kayıt seçebilir ve bunlar üzerinde işlem gerçekleştirebilir. Şirketler arası izin görünümü etkinse bu liste, erişimi olan tüm tüzel kişilikler genelinde bekleyen izin isteklerini gösterir. Aksi takdirde, seçili durumdaki tüzel kişilik için bekleyen izin isteklerini gösterir. </br>
 - **Tüm çalışanlar**: Bu sekme, İzin hiyerarşisinde devamsızlık yöneticisine atanan tüm çalışanları listeler. Her çalışan için kullanılabilen birkaç seçenek vardır:
    - **İzin isteme**: Seçili çalışan için yeni bir izin isteği gönderin.</br>
    - **İzin**: Seçili personel için bakiyeleri, onaylanmış izinleri ve izin isteklerini görüntüleyin.</br>

## <a name="approve-time-off-requests"></a>İzin isteklerini onaylama

Devamsızlık yöneticileri, personelin izin isteklerini onaylayabilir veya reddedebilir. 

> [!IMPORTANT]
> Devamsızlık yöneticilerinin izin isteklerini onaylaması veya reddetmesi için izin isteği iş akışının izin isteği alışma öğelerinin gözden geçirilmek üzere yöneticilere atanacak şekilde yapılandırılması gerekir.
>
> 1. **İnsan kaynakları iş akışları** sayfasında, izin isteği iş akışını seçin veya oluşturun.
> 2. **Hiyerarşiyi ilişkilendir** seçeneğini belirleyin ve **Hiyerarşi adı** alanında **İzin**'i seçin.
> 3. İş akışı tasarımcısında iş akışını güncelleştirin. **Atama türü** altında, **Hiyerarşi** seçeneğini belirleyin ve **Hiyerarşi seçimi** sekmesindeki **Yapılandırılabilir hiyerarşi**'yi seçin.
>
> İzin isteği iş akışını oluşturma hakkında bilgi için bkz. [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md).

1. **Çalışan self servisi** çalışma alanında, **İzin yönetimi** sekmesini seçin.

2. **İzin istekleri** sekmesinde, işlem yapmak istediğiniz izin isteklerini seçin. Bu liste görünümünde birden fazla kayıt seçebilirsiniz.

3. İzin isteğini Onaylamak, Reddetmek veya Devretmek için ızgaranın üst kısmındaki eylem düğmelerini kullanın. 

Alternatif olarak, kullanıcı ayrıca soldaki **İzin istekleri** kutucuğunu kullanarak izin isteği iş öğelerinin listesine de gidebilir. 

## <a name="view-time-off-in-the-calendar"></a>İzni takvimde görüntüleme

Devamsızlık yöneticisi rolündeki kullanıcılar izin isteklerini takvimlerinde görüntüleyebilir. İzin takvimine erişmek için aşağıdaki adımları izleyin.

> [!IMPORTANT]
> Sistem yöneticisi, devamsızlık yöneticisi takvimi için görünüm seçeneklerini yapılandırmalıdır. **İzin ve devamsızlık parametreleri** sayfasında, **Takvim** sekmesinde, doğum günlerini, ayrıntı içermeyen devamsızlıkları, devamsızlıkları ve bekleyen izin isteklerini gizleme veya gösterme seçenekleri vardır. Takvim görünümü seçeneğini çalışan türüne göre filtreleme seçeneği de vardır.

1. **Personel self servisi** çalışma alanında, **İzin yönetimi**'ni ve ardından **Devamsızlık yöneticisi takvimi**'ni seçin.

2. **Tarih** alanına istediğiniz tarihleri girin.

3. Görünüm seçeneklerini gerektiği gibi güncelleştirin.

Devamsızlık yöneticisi takvimi, İzin hiyerarşisinde devamsızlık yöneticisine rapor veren çalışanların tüm kayıtlarını gösterir.

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md)
- [Takım ve şirket takvimlerini görüntüleme](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
