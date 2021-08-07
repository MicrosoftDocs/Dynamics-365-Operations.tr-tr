---
title: Devamsızlık yöneticisi rolünü yapılandırma
description: Bu konuda, çalışan izninin yönetimi için Devamsızlık yöneticisi rolünün nasıl ayarlanacağı açıklanmaktadır.
author: hasrivas
ms.date: 07/19/2021
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
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639618"
---
# <a name="configure-the-absence-manager-role"></a>Devamsızlık yöneticisi rolünü yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Bazı kuruluşlarda, çalışan yöneticileri ekiplerinin iznini yönetmeyebilir. Bunun yerine, devamsızlık yöneticisi bu işlemi birden çok departman ve takımdaki ekip üyeleri için işleyebilir. Devamsızlık yöneticileri izin yönetimi için aşağıdaki özelliklere sahiptir:

- Alternatif bir hiyerarşiye göre izin süresini gözden geçirin ve onaylayın.
- Takım üyesi bakiyelerini görüntüleyin.
- Devamsızlık takvimini görüntüleyin.

## <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

1. **Sistem yönetimi** çalışma alanında **Özellik yönetimi**'ni seçin.

2. **Özellik yönetimi** sekmesinde, **(Önizleme) İzinleri devamsızlık yöneticisi yönetsin** özelliğini etkinleştirin.

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

İzin taleplerini onaylamalarını veya reddetmelerini sağlamak için personele Devamsızlık yöneticisi rolü atanmalıdır.

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

**Çalışan Self Servisi** çalışma alanında, **Devamsızlık yöneticisi** sekmesi, İzin hiyerarşisinde devamsızlık yöneticisine atanan personelle ilgili devamsızlık bilgilerini gösterir.

**İzin ve devamsızlık** sekmesinde, her çalışan için aşağıdaki seçenekler kullanılabilir:

- **İzin**: Seçili personel için bakiyeleri, onaylanmış izinleri ve izin taleplerini görüntüleyin.
- **İzin bakiyeleri**: Seçili personelin farklı izin planları için bakiyelerin listesini görüntüleyin.

## <a name="approve-time-off-requests"></a>İzin taleplerini onaylama

Devamsızlık yöneticileri, personelin izin taleplerini onaylayabilir veya reddedebilir. Gerektiğinde personel adına da talep oluşturabilirler.

> [!IMPORTANT]
> Devamsızlık yöneticilerinin izin talaplerini onaylaması veya reddetmesi için izin talebi iş akışının izin talebi çalışma öğelerinin gözden geçirilmek üzere yöneticilere atanacak şekilde yapılandırılması gerekir.
>
> 1. **İnsan kaynakları iş akışları** sayfasında, izin talebi iş akışını seçin veya oluşturun.
> 2. **Hiyerarşiyi ilişkilendir** seçeneğini belirleyin ve **Hiyerarşi adı** alanında **İzin**'i seçin.
> 3. İş akışı tasarımcısında iş akışını güncelleştirin. **Atama türü** altında, **Hiyerarşi** seçeneğini belirleyin ve **Hiyerarşi seçimi** sekmesindeki **Yapılandırılabilir hiyerarşi**'yi seçin.
>
> İzin talebi iş akışını oluşturma hakkında bilgi için bkz. [İzin talebi iş akışı oluşturma](hr-leave-and-absence-workflow.md).

1. **Çalışan Self Servisi** çalışma alanında **Devamsızlık yöneticisi** sekmesini seçin.

2. **Devamsızlık yöneticisi** sekmesinde, istediğiniz çalışanı seçin.

3. **Ayrıntılar**'ı seçin ve sonra **İzin**'i seçin.

4. İzin talebini bulun ve **Onay** seçeneğini belirleyin. Daha sonra izin talebini onaylamak veya iptal etmek için bir seçenek belirleyebilirsiniz.

**İptal** durumu, talebin reddedildiğini gösterir. **Tamamlandı** durumu, talebin onaylandığını gösterir.

## <a name="view-time-off-in-the-calendar"></a>İzni takvimde görüntüleme

Devamsızlık yöneticisi rolündeki kullanıcılar izin taleplerini takvimlerinde görüntüleyebilir. İzin takvimine erişmek için aşağıdaki adımları izleyin.

> [!IMPORTANT]
> Sistem yöneticisi, devamsızlık yöneticisi takvimi için görünüm seçeneklerini yapılandırmalıdır. **İzin ve devamsızlık parametreleri** sayfasında, **Takvim** sekmesinde, doğum günlerini, ayrıntı içermeyen devamsızlıkları, devamsızlıkları ve bekleyen izin taleplerini gizleme veya gösterme seçenekleri vardır. Takvim görünümü seçeneğini çalışan türüne göre filtreleme seçeneği de vardır.

1. **Çalışan Self Servisi** çalışma alanında **Devamsızlık yöneticisi**'ni ve ardından **Devamsızlık yöneticisi takvimi**'ni seçin.

2. **Tarih** alanına istediğiniz tarihleri girin.

3. Görünüm seçeneklerini gerektiği gibi güncelleştirin.

Devamsızlık yöneticisi takvimi, İzin hiyerarşisinde devamsızlık yöneticisine rapor veren çalışanların tüm kayıtlarını gösterir.

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md)
- [Takım ve şirket takvimlerini görüntüleme](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
