echo "# Pamela-Luana" >> README.md 
git init 
git add README.md 
git commit -m "primeiro commit" 
git branch -M main 
git remote add origin https://github.com/pamelanerisreis-hub/Pamela-Luana.git 
git push -u origin main
import 'package:shelf/.dart'
import'package:shelf/shelf_io.dart'as shelf-io;

void main()async{
  final handler=(Request request){
    return Response.ok('servidor funcionando!');
  };
  
  final server = await shelf_io.serve(
    handler,
    'localhost',
    8080,
  );
  print('servidor iniciado em http//\({server.address.host}:\){server.port}');
}
