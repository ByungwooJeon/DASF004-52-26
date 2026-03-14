## 1. 제출 정보

| 구분 | 내용 |
| --- | --- |
| 학년학기 | 2026학년도 1학기 |
| 과목명(학수번호) | 프로그래밍기초와실습 (DASF004-52) |
| 학번 | 2026310955 |
| 이름 | 전병우 |
| 과제명 | 심화실습-1 |

## 2. 현재 상태

### 2.1 배운적 있는 언어 및 현재 수준

- Python - 해당없음
- Java - 해당없음
- C - 해당없음

### 2.2 실습 환경

| 사용한AI 도구 | 개발환경 |
| --- | --- |
| Claude AI | GitHub Codespace |

## 3. 코드 리뷰 결과

### 3.1 AI가 생성한 코드를 얼마나 이해할 수 있었는지?

- 이해도: 6점
- 우선 글자 수 등과 같은 기본적인 규칙을 정하고, 각 데이터를 정의한 후 프로그램을 설계하는 방식으로 동작되는 것으로 이해했습니다.

### 3.2 최초에 입력한 프롬프트와 그 결과물에 대한 평가

#### 최초 프롬프트

```
일정관리 프로그램을 만들어줘.
일정 추가 기능이 있어야 하고 제목, 날짜, 시간, 설명을 입력할 수 있어야해.
그리고 일정 조회 기능이 있어야 하며 전체 일정 목록을 볼 수 있어야 해.
일정 수정 기능이 있어야 하고 기존 일정 정보를 변경할 수 있어야 해.
일정 삭제 기능이 있어야 하고 선택한 일정을 제거할 수 있어야 해.
이 프로그램은 한 개의 .c 파일에 C언어로 구현되어야 하며
키워드로 일정을 찾을 수 있는 일정 검색 기능과 날짜순으로 일정을 정렬할 수 있는 날짜별 정렬 기능, 파일 저장/불러오기로 일정 데이터를 영구 저장할 수 있는 기능도 있어야 해
```

#### 최종 코드 및 실행 결과

> 본 문서 가장 아래 `부록` 섹션에서 `최종 결과물 코드`와 `실행 결과`에 각각 코드 및 실행 결과를 복사 & 붙여넣기로 첨부합니다.

### 3.3 최종 결과물을 얻기까지의 경험

- 이러한 바이브 코딩이 처음이기 때문에 오류 발생 가능성을 줄이기 위해 강의 내용과 거의 동일하게 AI에게 요구할 수 있도록 하였습니다.
- 바이브 코딩으로 만든 코드를 원활히 실행시킬 수 있도록 1주차 강의를 다시 확인하며 실행하였습니다.
- 그래서 오류 없이 진행할 수 있었습니다.

## 4. 결론

- 코드 분석 과정에서 어려웠던 점은 대부분의 코드나 명령어가 아직 미숙한 상태이기 때문에 하나하나 재검토하는 과정입니다.
- 그래도 바이브코딩에 사용한 AI에게 다시 질문하며 코드에 대해 분석이 가능하였습니다.
- 당초 저에게 프로그래밍은 멀게 느껴졌었지만, AI를 활용하여 이러한 프로그래밍이 가능하다는 것을 배우고 머지않아 바이브코딩의 활용은 모두에게 필수적인 요소가 될 것 같다는 생각이 들었습니다.

## 참고문헌

- 클로드 AI를 활용하였고, 코드 분석도 해당 AI의 도움을 받았습니다.

--- 
---

## 부록

### 실행 결과

- 프로그램의 주요 기능 실행 화면을 터미널에서 텍스트를 복사&붙여넣기로 작성
- 프로그램 실행에 실패했다면, 실패와 관련된 내용을 담아도 좋음

```bash
@ByungwooJeon ➜ /workspaces/DASF004-52-26 (main) $ gcc assginment-1.c
assginment-1.c: In function ‘addSchedule’:
assginment-1.c:118:9: warning: ‘fgets’ writing 13 bytes into a region of size 11 overflows the destination [-Wstringop-overflow=]
  118 |         fgets(s.date, MAX_DATE + 2, stdin);
      |         ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
assginment-1.c:16:10: note: destination object ‘date’ of size 11
   16 |     char date[MAX_DATE];
      |          ^~~~
In file included from assginment-1.c:1:
/usr/include/stdio.h:654:14: note: in a call to function ‘fgets’ declared with attribute ‘access (write_only, 1, 2)’
  654 | extern char *fgets (char *__restrict __s, int __n, FILE *__restrict __stream)
      |              ^~~~~
assginment-1.c:126:9: warning: ‘fgets’ writing 8 bytes into a region of size 6 overflows the destination [-Wstringop-overflow=]
  126 |         fgets(s.time, MAX_TIME + 2, stdin);
      |         ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
assginment-1.c:17:10: note: destination object ‘time’ of size 6
   17 |     char time[MAX_TIME];
      |          ^~~~
/usr/include/stdio.h:654:14: note: in a call to function ‘fgets’ declared with attribute ‘access (write_only, 1, 2)’
  654 | extern char *fgets (char *__restrict __s, int __n, FILE *__restrict __stream)
      |              ^~~~~
@ByungwooJeon ➜ /workspaces/DASF004-52-26 (main) $ gcc ./a.out
/usr/bin/ld: input file './a.out' is the same as output file
collect2: error: ld returned 1 exit status
@ByungwooJeon ➜ /workspaces/DASF004-52-26 (main) $ ./a.out
  일정 관리 프로그램을 시작합니다.
  저장된 파일이 없습니다. 새로 시작합니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 1

  ── 일정 추가 ──
  제목    : 개강총회
  날짜 (YYYY-MM-DD) : 2026-03-14
  시간 (HH:MM)      : 18:00
  설명    : 성대지붕
  ✔  일정이 추가되었습니다. (ID: 1)
  ✔  'schedules.dat' 파일에 1개의 일정이 저장되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 1

  ── 일정 추가 ──
  제목    : 학생회 면접
  날짜 (YYYY-MM-DD) : 2026-03-15
  시간 (HH:MM)      : 17:30
  설명    : 인사캠
  ✔  일정이 추가되었습니다. (ID: 2)
  ✔  'schedules.dat' 파일에 2개의 일정이 저장되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 1

  ── 일정 추가 ──
  제목    : 과제제출
  날짜 (YYYY-MM-DD) : 2026-03-16
  시간 (HH:MM)      : 09:00
  설명    : 프기실 심화학습01 
  ✔  일정이 추가되었습니다. (ID: 3)
  ✔  'schedules.dat' 파일에 3개의 일정이 저장되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 2

  ── 전체 일정 목록 (3개) ──
════════════════════════════════════════════════════════════
  [ID: 1]
  제목    : 개강총회
  날짜    : 2026-03-14
  시간    : 18:00
  설명    : 성대지붕
════════════════════════════════════════════════════════════
  [ID: 2]
  제목    : 학생회 면접
  날짜    : 2026-03-15
  시간    : 17:30
  설명    : 인사캠
════════════════════════════════════════════════════════════
  [ID: 3]
  제목    : 과제제출
  날짜    : 2026-03-16
  시간    : 09:00
  설명    : 프기실 심화학습01
════════════════════════════════════════════════════════════

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 3

  수정할 일정 ID: 3
  현재 제목 [과제제출] → 새 제목 (변경 없으면 Enter): 
  현재 날짜 [2026-03-16] → 새 날짜 (변경 없으면 Enter): 
  현재 시간 [09:00] → 새 시간 (변경 없으면 Enter): 08:50
  현재 설명 [프기실 심화학습01] → 새 설명 (변경 없으면 Enter): 
  ✔  일정이 수정되었습니다.
  ✔  'schedules.dat' 파일에 3개의 일정이 저장되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 4

  삭제할 일정 ID: 2
  삭제할 일정:
  [ID: 2]
  제목    : 학생회 면접
  날짜    : 2026-03-15
  시간    : 17:30
  설명    : 인사캠
  정말 삭제하시겠습니까? (y/n):  y
  ✔  일정이 삭제되었습니다.
  ✔  'schedules.dat' 파일에 2개의 일정이 저장되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 2

  ── 전체 일정 목록 (2개) ──
════════════════════════════════════════════════════════════
  [ID: 1]
  제목    : 개강총회
  날짜    : 2026-03-14
  시간    : 18:00
  설명    : 성대지붕
════════════════════════════════════════════════════════════
  [ID: 3]
  제목    : 과제제출
  날짜    : 2026-03-16
  시간    : 08:50
  설명    : 프기실 심화학습01
════════════════════════════════════════════════════════════

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 5

  검색 키워드: 과제 

  ── 검색 결과 (키워드: "과제") ──
════════════════════════════════════════════════════════════
  [ID: 3]
  제목    : 과제제출
  날짜    : 2026-03-16
  시간    : 08:50
  설명    : 프기실 심화학습01
════════════════════════════════════════════════════════════
  총 1개의 일정이 검색되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 6
  ✔  날짜 및 시간 순서로 정렬되었습니다.
  ✔  'schedules.dat' 파일에 2개의 일정이 저장되었습니다.

  ── 전체 일정 목록 (2개) ──
════════════════════════════════════════════════════════════
  [ID: 1]
  제목    : 개강총회
  날짜    : 2026-03-14
  시간    : 18:00
  설명    : 성대지붕
════════════════════════════════════════════════════════════
  [ID: 3]
  제목    : 과제제출
  날짜    : 2026-03-16
  시간    : 08:50
  설명    : 프기실 심화학습01
════════════════════════════════════════════════════════════

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 7
  ✔  'schedules.dat' 파일에 2개의 일정이 저장되었습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 8
  ✔  'schedules.dat' 파일에서 2개의 일정을 불러왔습니다.

════════════════════════════════════════════════════════════
          📅  일정 관리 프로그램
════════════════════════════════════════════════════════════
  1. 일정 추가
  2. 전체 일정 조회
  3. 일정 수정
  4. 일정 삭제
  5. 일정 검색
  6. 날짜순 정렬
  7. 파일 저장
  8. 파일 불러오기
  0. 종료
════════════════════════════════════════════════════════════
  선택: 0
  프로그램을 종료합니다.
```

### 최종 결과물 코드

- AI가 생성한 전체 코드 첨부

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_TITLE       100
#define MAX_DATE        11   /* YYYY-MM-DD */
#define MAX_TIME        6    /* HH:MM */
#define MAX_DESC        500
#define MAX_SCHEDULES   1000
#define DATA_FILE       "schedules.dat"

/* ───────────────────────── 구조체 ───────────────────────── */
typedef struct {
    int  id;
    char title[MAX_TITLE];
    char date[MAX_DATE];
    char time[MAX_TIME];
    char desc[MAX_DESC];
} Schedule;

/* ───────────────────────── 전역 변수 ───────────────────────── */
Schedule schedules[MAX_SCHEDULES];
int      count      = 0;
int      nextId     = 1;

/* ───────────────────────── 유틸리티 ───────────────────────── */
void clearInputBuffer(void) {
    int c;
    while ((c = getchar()) != '\n' && c != EOF);
}

void printSeparator(void) {
    printf("════════════════════════════════════════════════════════════\n");
}

void printSchedule(const Schedule *s) {
    printf("  [ID: %d]\n", s->id);
    printf("  제목    : %s\n", s->title);
    printf("  날짜    : %s\n", s->date);
    printf("  시간    : %s\n", s->time);
    printf("  설명    : %s\n", s->desc);
}

/* 날짜 형식 검증 (YYYY-MM-DD) */
int isValidDate(const char *date) {
    if (strlen(date) != 10) return 0;
    if (date[4] != '-' || date[7] != '-') return 0;
    int y, m, d;
    if (sscanf(date, "%d-%d-%d", &y, &m, &d) != 3) return 0;
    if (m < 1 || m > 12 || d < 1 || d > 31) return 0;
    return 1;
}

/* 시간 형식 검증 (HH:MM) */
int isValidTime(const char *t) {
    if (strlen(t) != 5) return 0;
    if (t[2] != ':') return 0;
    int h, m;
    if (sscanf(t, "%d:%d", &h, &m) != 2) return 0;
    if (h < 0 || h > 23 || m < 0 || m > 59) return 0;
    return 1;
}

/* ID로 인덱스 찾기 */
int findIndexById(int id) {
    for (int i = 0; i < count; i++)
        if (schedules[i].id == id) return i;
    return -1;
}

/* ───────────────────────── 파일 저장/불러오기 ───────────────────────── */
void saveToFile(void) {
    FILE *fp = fopen(DATA_FILE, "wb");
    if (!fp) {
        printf("  [오류] 파일 저장에 실패했습니다.\n");
        return;
    }
    fwrite(&count,  sizeof(int), 1, fp);
    fwrite(&nextId, sizeof(int), 1, fp);
    fwrite(schedules, sizeof(Schedule), count, fp);
    fclose(fp);
    printf("  ✔  '%s' 파일에 %d개의 일정이 저장되었습니다.\n", DATA_FILE, count);
}

void loadFromFile(void) {
    FILE *fp = fopen(DATA_FILE, "rb");
    if (!fp) {
        printf("  저장된 파일이 없습니다. 새로 시작합니다.\n");
        return;
    }
    fread(&count,  sizeof(int), 1, fp);
    fread(&nextId, sizeof(int), 1, fp);
    fread(schedules, sizeof(Schedule), count, fp);
    fclose(fp);
    printf("  ✔  '%s' 파일에서 %d개의 일정을 불러왔습니다.\n", DATA_FILE, count);
}

/* ───────────────────────── 기능 함수 ───────────────────────── */

/* 1. 일정 추가 */
void addSchedule(void) {
    if (count >= MAX_SCHEDULES) {
        printf("  [오류] 저장 가능한 일정 수를 초과했습니다.\n");
        return;
    }
    Schedule s;
    s.id = nextId++;

    printf("\n  ── 일정 추가 ──\n");

    printf("  제목    : ");
    fgets(s.title, MAX_TITLE, stdin);
    s.title[strcspn(s.title, "\n")] = '\0';
    if (strlen(s.title) == 0) { printf("  [오류] 제목은 필수입니다.\n"); nextId--; return; }

    do {
        printf("  날짜 (YYYY-MM-DD) : ");
        fgets(s.date, MAX_DATE + 2, stdin);
        s.date[strcspn(s.date, "\n")] = '\0';
        if (!isValidDate(s.date))
            printf("  [오류] 올바른 날짜 형식이 아닙니다. 다시 입력하세요.\n");
    } while (!isValidDate(s.date));

    do {
        printf("  시간 (HH:MM)      : ");
        fgets(s.time, MAX_TIME + 2, stdin);
        s.time[strcspn(s.time, "\n")] = '\0';
        if (!isValidTime(s.time))
            printf("  [오류] 올바른 시간 형식이 아닙니다. 다시 입력하세요.\n");
    } while (!isValidTime(s.time));

    printf("  설명    : ");
    fgets(s.desc, MAX_DESC, stdin);
    s.desc[strcspn(s.desc, "\n")] = '\0';

    schedules[count++] = s;
    printf("  ✔  일정이 추가되었습니다. (ID: %d)\n", s.id);
    saveToFile();
}

/* 2. 전체 일정 조회 */
void listSchedules(void) {
    printf("\n  ── 전체 일정 목록 (%d개) ──\n", count);
    if (count == 0) {
        printf("  등록된 일정이 없습니다.\n");
        return;
    }
    for (int i = 0; i < count; i++) {
        printSeparator();
        printSchedule(&schedules[i]);
    }
    printSeparator();
}

/* 3. 일정 수정 */
void editSchedule(void) {
    if (count == 0) { printf("  등록된 일정이 없습니다.\n"); return; }

    int id;
    printf("\n  수정할 일정 ID: ");
    if (scanf("%d", &id) != 1) { clearInputBuffer(); return; }
    clearInputBuffer();

    int idx = findIndexById(id);
    if (idx < 0) { printf("  [오류] 해당 ID의 일정을 찾을 수 없습니다.\n"); return; }

    Schedule *s = &schedules[idx];
    char buf[MAX_DESC];

    printf("  현재 제목 [%s] → 새 제목 (변경 없으면 Enter): ", s->title);
    fgets(buf, MAX_TITLE, stdin);
    buf[strcspn(buf, "\n")] = '\0';
    if (strlen(buf) > 0) strncpy(s->title, buf, MAX_TITLE - 1);

    printf("  현재 날짜 [%s] → 새 날짜 (변경 없으면 Enter): ", s->date);
    fgets(buf, MAX_DATE + 2, stdin);
    buf[strcspn(buf, "\n")] = '\0';
    if (strlen(buf) > 0) {
        if (isValidDate(buf)) strncpy(s->date, buf, MAX_DATE - 1);
        else printf("  [경고] 날짜 형식 오류로 변경되지 않았습니다.\n");
    }

    printf("  현재 시간 [%s] → 새 시간 (변경 없으면 Enter): ", s->time);
    fgets(buf, MAX_TIME + 2, stdin);
    buf[strcspn(buf, "\n")] = '\0';
    if (strlen(buf) > 0) {
        if (isValidTime(buf)) strncpy(s->time, buf, MAX_TIME - 1);
        else printf("  [경고] 시간 형식 오류로 변경되지 않았습니다.\n");
    }

    printf("  현재 설명 [%s] → 새 설명 (변경 없으면 Enter): ", s->desc);
    fgets(buf, MAX_DESC, stdin);
    buf[strcspn(buf, "\n")] = '\0';
    if (strlen(buf) > 0) strncpy(s->desc, buf, MAX_DESC - 1);

    printf("  ✔  일정이 수정되었습니다.\n");
    saveToFile();
}

/* 4. 일정 삭제 */
void deleteSchedule(void) {
    if (count == 0) { printf("  등록된 일정이 없습니다.\n"); return; }

    int id;
    printf("\n  삭제할 일정 ID: ");
    if (scanf("%d", &id) != 1) { clearInputBuffer(); return; }
    clearInputBuffer();

    int idx = findIndexById(id);
    if (idx < 0) { printf("  [오류] 해당 ID의 일정을 찾을 수 없습니다.\n"); return; }

    printf("  삭제할 일정:\n");
    printSchedule(&schedules[idx]);
    printf("  정말 삭제하시겠습니까? (y/n): ");
    char ch = getchar(); clearInputBuffer();
    if (ch != 'y' && ch != 'Y') { printf("  삭제가 취소되었습니다.\n"); return; }

    for (int i = idx; i < count - 1; i++)
        schedules[i] = schedules[i + 1];
    count--;
    printf("  ✔  일정이 삭제되었습니다.\n");
    saveToFile();
}

/* 5. 키워드 검색 */
void searchSchedules(void) {
    char keyword[MAX_TITLE];
    printf("\n  검색 키워드: ");
    fgets(keyword, MAX_TITLE, stdin);
    keyword[strcspn(keyword, "\n")] = '\0';

    int found = 0;
    printf("\n  ── 검색 결과 (키워드: \"%s\") ──\n", keyword);
    for (int i = 0; i < count; i++) {
        if (strstr(schedules[i].title, keyword) ||
            strstr(schedules[i].desc,  keyword) ||
            strstr(schedules[i].date,  keyword)) {
            printSeparator();
            printSchedule(&schedules[i]);
            found++;
        }
    }
    if (found == 0) printf("  검색 결과가 없습니다.\n");
    else { printSeparator(); printf("  총 %d개의 일정이 검색되었습니다.\n", found); }
}

/* 6. 날짜순 정렬 (버블 정렬) */
void sortByDate(void) {
    if (count < 2) { printf("  정렬할 일정이 충분하지 않습니다.\n"); return; }

    for (int i = 0; i < count - 1; i++) {
        for (int j = 0; j < count - 1 - i; j++) {
            int cmp = strcmp(schedules[j].date, schedules[j+1].date);
            if (cmp > 0 || (cmp == 0 &&
                strcmp(schedules[j].time, schedules[j+1].time) > 0)) {
                Schedule tmp      = schedules[j];
                schedules[j]      = schedules[j+1];
                schedules[j+1]    = tmp;
            }
        }
    }
    printf("  ✔  날짜 및 시간 순서로 정렬되었습니다.\n");
    saveToFile();
    listSchedules();
}

/* ───────────────────────── 메인 메뉴 ───────────────────────── */
void printMenu(void) {
    printf("\n");
    printSeparator();
    printf("          📅  일정 관리 프로그램\n");
    printSeparator();
    printf("  1. 일정 추가\n");
    printf("  2. 전체 일정 조회\n");
    printf("  3. 일정 수정\n");
    printf("  4. 일정 삭제\n");
    printf("  5. 일정 검색\n");
    printf("  6. 날짜순 정렬\n");
    printf("  7. 파일 저장\n");
    printf("  8. 파일 불러오기\n");
    printf("  0. 종료\n");
    printSeparator();
    printf("  선택: ");
}

int main(void) {
    printf("  일정 관리 프로그램을 시작합니다.\n");
    loadFromFile();

    int choice;
    while (1) {
        printMenu();
        if (scanf("%d", &choice) != 1) { clearInputBuffer(); continue; }
        clearInputBuffer();

        switch (choice) {
            case 1: addSchedule();    break;
            case 2: listSchedules();  break;
            case 3: editSchedule();   break;
            case 4: deleteSchedule(); break;
            case 5: searchSchedules();break;
            case 6: sortByDate();     break;
            case 7: saveToFile();     break;
            case 8: loadFromFile();   break;
            case 0:
                printf("  프로그램을 종료합니다.\n");
                return 0;
            default:
                printf("  [오류] 올바른 메뉴 번호를 입력하세요.\n");
        }
    }
    return 0;
}
```
