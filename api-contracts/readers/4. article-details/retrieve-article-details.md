# API: Retrieve Article Details

### Use Cases
Use this endpoint to retrieve an article' full details, view images and multimedia content.

### URL
```
GET {baseUrl}/news/{slug}/
```
| Parameter | Type | Description                       |
|-----------|------|-----------------------------------|
| slug      | str  | The unique slug of the news feed. |


### Headers
```
Authorization: Bearer {jwt_token}
```

### Response Format
The API will return a `200 OK` with the below response body.

```
{
    "slug": "the-rise-of-covid-19",
    "title": "The rise of COVID-19 infection.",
    "short_description": "Coronavirus disease (COVID-19) is an infectious disease caused by the SARS-CoV-2 virus.",
    "image_url": "https://example.com/the-rise-of-covid-19.png",
    "external_news_url": "https://timesofindia.com/the-rise-of-covid-19",
    "category": {
        "slug": "medicine",
        "name": "Medicine"
    },
    "long_description": "Coronavirus disease (COVID-19) is an infectious disease caused by the SARS-CoV-2 virus. Most people infected with the virus will experience mild to moderate respiratory illness and recover without requiring special treatment. However, some will become seriously ill and require medical attention. Older people and those with underlying medical conditions like cardiovascular disease, diabetes, chronic respiratory disease, or cancer are more likely to develop serious illness. Anyone can get sick with COVID-19 and become seriously ill or die at any age. The best way to prevent and slow down transmission is to be well informed about the disease and how the virus spreads. Protect yourself and others from infection by staying at least 1 metre apart from others, wearing a properly fitted mask, and washing your hands or using an alcohol-based rub frequently. Get vaccinated when it’s your turn and follow local guidance. The virus can spread from an infected person’s mouth or nose in small liquid particles when they cough, sneeze, speak, sing or breathe. These particles range from larger respiratory droplets to smaller aerosols. It is important to practice respiratory etiquette, for example by coughing into a flexed elbow, and to stay home and self-isolate until you recover if you feel unwell.",
    "multimedia": [
        {
            "kind": "video",
            "multimedia_url": "https://youtube.com/kaer4i5uy"
        },
        {
            "kind": "pdf",
            "multimedia_url": "https://example.com/covid-19.pdf"
        }
    ]
}
```
