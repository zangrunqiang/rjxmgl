# rjxmgl
软件项目管理课程
import javax.swing.JOptionPane;
public class SubtractionTutorLoop{
public static void main(String[] args){
  int correctCount=0;
  int Count=0;
  long startTime=System.currentTimeMills();
  String output="";
  while(count<10){
  int number1=(int)(Math.random()*10);
  int number2=(int)(Math.random()*10);
  if(number1<number2){
  int temper=number1;
  number1=number2;
  number2=temper;
  }
  String answerString=JOptionPane.showInputDialog("what is"+number1+"-"+number2+"?");
  int answer=Integer.parseInt(answerString);
  String replyString;
  if(number1-number2==answer){
  replyString="you are right";
  correctCount++;
  }
  else replyString="your answer is wrong.\n"+number1+"-"+number2+"should be"+(number1-number2);
  JOptionPane.showMessageDialog(null,replyString);
  count++;
  output+="\n"+number1+"-"+number+"="+answerString+((number1-number2==answer)?"correct":"wrong");
  }
  long endTime=System.currentTimeMills();
  long testTime=endTime-startTime;
  JOptionPane.showMessageDialog(null,"correct count is"+correctCount+"\nTest time is"+testTime/1000+"Second\n"+output);
  }
  }
