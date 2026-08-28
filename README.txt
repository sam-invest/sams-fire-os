Sam's FIRE OS Web v5.1 — Supabase Cloud Sync

배포: GitHub 저장소의 기존 v5.0 파일을 이 ZIP의 파일들로 교체한 뒤 Commit 합니다. GitHub Pages는 자동으로 다시 배포됩니다.

로그인: Supabase Authentication > Users에서 만든 이메일/비밀번호 계정을 사용합니다. 기존 capion/182182 브라우저 로그인은 제거되었습니다.

최초 동기화:
1) 기존 v5.0 실제 자료가 들어 있는 PC 브라우저에서 먼저 v5.1 사이트를 엽니다.
2) Supabase 계정으로 로그인합니다.
3) 클라우드에 자료가 아직 없으면 현재 PC의 로컬 FIRE OS 자료가 최초 업로드됩니다.
4) 이후 휴대폰/다른 PC에서 같은 계정으로 로그인하면 클라우드 자료를 불러옵니다.

보안: publishable key만 웹앱에 포함됩니다. service_role/secret key/DB password는 포함하지 않습니다. fire_os_data 테이블은 RLS 정책으로 로그인한 본인의 user_id 행만 접근하도록 구성되어야 합니다.

오프라인: 로컬 저장은 계속 유지됩니다. 인터넷 연결이 없으면 로컬 자료를 사용할 수 있으며 클라우드 저장은 연결 후 다음 저장 시 재시도됩니다.
