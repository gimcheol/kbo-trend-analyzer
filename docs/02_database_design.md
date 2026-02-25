# Database Design

## 1. 설계 원칙

- 계산 가능한 값(OPS, ERA)은 DB에 저장하지 않는다.
- 시즌 기록과 경기 기록을 분리한다.
- 확장 가능성을 고려하여 팀 엔티티를 분리한다.

---

## 2. ERD 개요

### Player
- id (PK)
- name
- team_id (FK)
- position
- back_number
- birth_date

### Team
- id (PK)
- name
- founded_year

### HitterSeasonStats
- id (PK)
- player_id (FK)
- season
- games
- at_bats
- hits
- home_runs
- walks

### PitcherSeasonStats
- id (PK)
- player_id (FK)
- season
- innings
- earned_runs
- strikeouts
- walks

### GameStats
- id (PK)
- player_id (FK)
- game_date
- at_bats
- hits
- earned_runs
- innings
  
