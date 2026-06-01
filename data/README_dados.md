# Dataset — Divvy Trips 2019

## Como baixar

O dataset oficial está disponível publicamente em:

👉 **https://divvy-tripdata.s3.amazonaws.com/index.html**

## Arquivos necessários

Baixe os 4 arquivos trimestrais de 2019 e salve nesta pasta (`data/`):

| Arquivo | Período | Link direto |
|---------|---------|-------------|
| `Divvy_Trips_2019_Q1.zip` | Jan-Mar 2019 | https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q1.zip |
| `Divvy_Trips_2019_Q2.zip` | Abr-Jun 2019 | https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q2.zip |
| `Divvy_Trips_2019_Q3.zip` | Jul-Set 2019 | https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q3.zip |
| `Divvy_Trips_2019_Q4.zip` | Out-Dez 2019 | https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q4.zip |

## Estrutura do dataset

| Coluna | Descrição |
|--------|-----------|
| `trip_id` | ID único da viagem |
| `start_time` | Data e hora de início |
| `end_time` | Data e hora de fim |
| `bikeid` | ID da bicicleta |
| `tripduration` | Duração em segundos |
| `from_station_id` | ID da estação de origem |
| `from_station_name` | Nome da estação de origem |
| `to_station_id` | ID da estação de destino |
| `to_station_name` | Nome da estação de destino |
| `usertype` | `Subscriber` (membro) ou `Customer` (casual) |
| `gender` | Gênero (apenas membros) |
| `birthyear` | Ano de nascimento (apenas membros) |

## Licença

Dados licenciados pela **Lyft Bikes and Scooters, LLC** sob a  
[Divvy Data License Agreement](https://divvybikes.com/data-license-agreement).

Os dados são públicos e disponibilizados para análise não-comercial.
