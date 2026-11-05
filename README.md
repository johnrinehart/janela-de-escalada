# Janela de Escalada

Previsão de chuva para picos de escalada, focada no que importa para decidir onde escalar no fim de semana: **chance de chuva (%)** e **milímetros** por dia, além de um aviso de rocha úmida quando choveu nos dois dias anteriores.

- **Picos:** uma grade com os próximos dias (ou só os fins de semana), com os picos ordenados pela distância até você.
- **Mapa da viagem:** você escolhe ida e volta e vê a chance máxima e a chuva total de cada pico no período.

Previsão do [Open-Meteo](https://open-meteo.com/) (gratuito, sem chave). Mapa com Leaflet + OpenStreetMap.

## Cadastrar ou editar picos

Edite [`picos.json`](picos.json) e faça push. Cada pico:

```json
{ "id": "bau", "name": "Pedra do Baú", "region": "São Bento do Sapucaí, SP", "lat": -22.6870, "lon": -45.6600 }
```

`id` precisa ser único. As coordenadas de exemplo são aproximadas.

## Rodar localmente

O `picos.json` é carregado via `fetch`, então abra por um servidor HTTP em vez de abrir o arquivo direto:

```bash
python -m http.server 8765
```

e acesse http://localhost:8765.
