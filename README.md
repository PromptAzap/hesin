# 🕌 HESIN - منظومة المعرفة الإسلامية المنهجية

**Hierarchical Educational System for Islamic Knowledge**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Arabic](https://img.shields.io/badge/العربية-محتوى-green.svg)](README.md)
[![Ontology](https://img.shields.io/badge/Ontology-JSON-blue.svg)]()

## 📖 عن المشروع

**HESIN** هو مستودع معرفي ضخم يحتوي على منظومة متكاملة من المفاهيم الإسلامية المنهجية المستخلصة من دروس العلامة **السيد/ حسين بدر الدين الحوثي** (رحمه الله). يمثل المشروع قاعدة معرفية منظمة على شكل **أنطولوجيا دلالية** (Semantic Ontology) تربط بين المفاهيم القرآنية والعقدية والتربوية عبر علاقات منطقية وسببية.

## 🎯 الهدف من المشروع

- 📚 توثيق التراث المعرفي الإسلامي بشكل منظم وآلي
- 🔗 بناء شبكة مفاهيمية مترابطة تسهل الفهم والاستدلال
- 💡 تمكين الباحثين والطلاب من الوصول للمعرفة بشكل منهجي
- 🤖 توفير قاعدة معرفية قابلة للاستخدام في الأنظمة الذكية والذكاء الاصطناعي
- 📊 تحليل الخطاب الديني بمنهجية علمية دقيقة

## 📂 هيكلية البيانات

### الملفات المتوفرة

| الملف | المفاهيم | الآيات | الأحاديث | السلاسل السببية |
|-------|---------|--------|----------|-----------------|
| **مفاهيم سلسلة ملازم المدرسة** | ~262 | ~50 | ~12 | - |
| **مفاهيم سلسلة دروس معرفة الله** | ~1,417 | ~40 | ~3 | ~15 |
| **مفاهيم سلسلة دروس من سورة المائدة** | ~126 | ~25 | - | ~5 |
| **مفاهيم سلسلة دروس مديح القرآن** | ~225 | ~30 | 1 | ~12 |
| **الإجمالي** | **~2,030** | **~145** | **~16** | **~32** |

### نموذج البيانات (JSON Schema)

كل ملف JSON يحتوي على الهيكلية التالية:

```json
{
  "collection": {
    "name": "اسم السلسلة",
    "description": "وصف السلسلة"
  },
  "lessons": [
    {
      "title": "عنوان الدرس",
      "author": "المؤلف",
      "methodology": "المنهجية المتبعة",
      "total_concepts": 0,
      "total_verses": 0,
      "total_hadiths": 0
    }
  ],
  "concepts": [
    {
      "concept_id_placeholder": "C001",
      "name": "اسم المفهوم",
      "synonyms": ["مرادفات"],
      "definition": "التعريف العملي",
      "components": ["المكونات"],
      "boundaries": "الحدود",
      "importance": "رئيسي/فرعي/هامشي",
      "confidence": "واضح/ضمني",
      "actions": "الإجراءات المنهجية",
      "foundational_quote": "النص المؤسس",
      "group_name": "المجموعة المفاهيمية"
    }
  ],
  "relations": [
    {
      "source_concept_id_placeholder": "C001",
      "target_concept_id_placeholder": "C002",
      "relation_type": "نوع العلاقة",
      "reason": "السبب"
    }
  ],
  "causal_chains": [
    {
      "chain_name": "اسم السلسلة",
      "description": "الوصف",
      "steps": [
        {
          "concept_id_placeholder": "C001",
          "step_order": 1,
          "notes": "ملاحظات"
        }
      ]
    }
  ],
  "verses": [
    {
      "surah": "اسم السورة",
      "verse_number": 0,
      "verse_text": "نص الآية",
      "related_concept_placeholders": ["C001"]
    }
  ],
  "hadiths": [
    {
      "narrator": "الراوي",
      "text": "نص الحديث",
      "source": "المصدر",
      "related_concept_placeholders": ["C001"]
    }
  ]
}
