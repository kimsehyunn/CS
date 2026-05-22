1. 의존성을 왜쓰는가? Nest.js 의존성 주입 방법
   
객체가 필요한 의존성을 직접 생성하지 않고 외부에서 주입받는 설계 기법입니다.
객체 간의 결합도를 낮추고 유연성과 재사용성을 높이며, 단위 테스트를 용이하게 만들기 위해 사용합니다.

Module
기능 단위로 묶는 기본 단위. 컨트롤러, 서비스 등을 포함
@Module({ controllers: [], providers: [] })


Controller
HTTP 요청을 받아 라우팅 처리
@Controller('user'), @Get()


Service
비즈니스 로직 담당. Controller와 분리
@Injectable() 사용


Decorator
클래스/메서드에 메타데이터를 부여
@Get(), @Param(), @Body() 등


Dependency Injection (DI)
의존 객체를 직접 생성하지 않고 자동 주입
생성자에 의존성 선언만으로 주입됨


Pipe
요청 데이터의 검증 및 변환
ValidationPipe, ParseIntPipe 등


Guard
요청 차단 또는 허용 (인증/권한 검사)
@UseGuards(AuthGuard('jwt'))


Interceptor
요청/응답을 가로채어 공통 처리 (로깅, 캐싱 등)
NestInterceptor 구현


Exception Filter
예외 발생 시 커스텀 응답 처리
@Catch(HttpException)


Middleware
요청 전 처리 로직 (로그, 인증 등)
Express 스타일 req, res, next 사용 


3. 인덱스를 최적화 

4. 동시성 문제란? 동시성 문제 해결 방법 

5. AWS
   Iam MSK Cloudfare Cloudwatch

6. AI harness engineerign

7. kafka
   https://aws.amazon.com/ko/what-is/apache-kafka/
