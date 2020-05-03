# java-generator
Generator Controller &amp; Service &amp; Entities using Postgres Table


####  Basic Config

`java

    @RunWith(SpringRunner.class)
    @SpringBootTest(classes = TestConfig.class)
    public class GeneratorTest {
    
        @Autowired
        DataSource dataSource;
    
        @Test
        @Ignore
        public void test() throws Exception {
    
            String rootPackage = this.getClass().getPackage().getName();
    
            String projectRoot = "/Users/i353584/Documents/SCH-Portal/Athena";
    
            JavaGenerator javaGenerator = JavaGeneratorBuilder.builder()
                    .connection(dataSource.getConnection())
                    .packageName(rootPackage)
                    .projectRoot(projectRoot)
                    .build();
    
        }
    }
`

#### Generate Dto Objects
