# Ejercicio-1.-Interfaz-de-usuario

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Ejercicio1TSPTheme {
                // A surface container using the 'background' color from the theme
                Surface(modifier = Modifier.fillMaxSize(), 
                    color = MaterialTheme.colorScheme.background) {
                    CertificatingCourse(" Yepez Cruz Diego Alberto ")
                }
            }
        }
    }
}

@Composable
fun CertificatingCourse(nombre: String, modifier: Modifier = Modifier) {
    Column(
        modifier = modifier
            .fillMaxSize()
            .padding(28.dp),
        verticalArrangement = Arrangement.Top

    ){
Row(
    modifier= Modifier.fillMaxWidth(),
    horizontalArrangement = Arrangement.SpaceBetween
){

        Image(painter = painterResource(id = R.drawable.video_game_1332694_640),
            contentDescription = null,
            modifier= Modifier
                .wrapContentHeight()
                .width(50.dp)
                .height(50.dp)
        )
    Image(painter = painterResource(id = R.drawable.kontroller_2022084_640__1_),
        contentDescription = null,
        modifier= Modifier
            .wrapContentHeight()
            .width(50.dp)
            .height(50.dp)
        )
}
        Text(text = "SONY",
            textAlign = TextAlign.Center,
            modifier= Modifier
                .fillMaxWidth()
                .padding(vertical = 15.dp),

            )

        Text(text = "This certificate is presented to: ",
            fontSize = 20.sp,
            //fontWeight =  FontWeight.Bold,
            textAlign = TextAlign.Center,
               modifier= modifier
                   .fillMaxWidth()
                   .padding(vertical = 8.dp)
        )

Box(modifier = modifier) {
    Text(
        text = "$nombre",
        fontSize = 32.sp,
        fontWeight = FontWeight.Bold,
        textAlign = TextAlign.Center,
        modifier = modifier
            .fillMaxWidth()
            .padding(vertical = 8.dp)

    )
}

            Text(
                text = "has completed 10 hours course on ",
                fontSize = 20.sp,
               textAlign = TextAlign.Center,
                modifier= Modifier
                    .fillMaxWidth()
                    .padding(vertical = 8.dp)
            )

        Text(text = " Pacman ",
            fontSize = 20.sp,
            textAlign= TextAlign.Center,
            modifier= Modifier.fillMaxWidth(),
            fontWeight =  FontWeight.Bold,

        )

    }
    Box(
        modifier = Modifier.fillMaxSize(),
        contentAlignment = Alignment.BottomCenter
    ) {
        Row(
            horizontalArrangement = Arrangement.SpaceAround,
            modifier = Modifier.fillMaxWidth()
        ) {
            Column(horizontalAlignment = Alignment.CenterHorizontally) {
                Image(
                    painter = painterResource(id = R.drawable.firma_1),
                    contentDescription = null,
                    modifier = Modifier
                        .width(150.dp)
                        .height(100.dp)
                )
                Text(
                    text = "General Manager",
                    fontSize = 16.sp,
                    textAlign = TextAlign.Center,
                    modifier = Modifier.padding(vertical = 8.dp)
                )
            }
            Column(horizontalAlignment = Alignment.CenterHorizontally) {
                Image(
                    painter = painterResource(id = R.drawable.firma2),
                    contentDescription = null,
                    modifier = Modifier
                        .width(150.dp)
                        .height(100.dp)
                )
                Text(
                    text = "Pacman Creator",
                    fontSize = 16.sp,
                    textAlign = TextAlign.Center,
                    modifier = Modifier.padding(vertical = 8.dp)
                )
            }
        }
    }
}
@Preview(showBackground = true)
@Composable
fun GreetingPreview() {
    Ejercicio1TSPTheme {
        CertificatingCourse("Android")
    }
}
