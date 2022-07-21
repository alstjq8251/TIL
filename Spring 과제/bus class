import java.util.*;
public class Bus extends Vehicle {
    protected String condition = "운행";
    protected int maxPassenger = 30;
    protected int price = 1000;
    protected int currentPassenger = 0;

    public Bus(int num) {
        super(num);

    }
    void getStatus(){
        System.out.println("번호: "+this.num);
        System.out.println("주유량: "+this.fuel);
        System.out.println("상태: "+this.condition+"\n");
    }


    void getFuel(int a) {
        this.fuel += a;
        if (this.fuel > 10) {
            System.out.println("주유량: " + this.fuel);
            System.out.println("상태: " + this.condition);
            System.out.println();
        } else if (this.fuel < 10) {
            this.condition = "차고지행";
            System.out.printf("주유량 : %d\n", this.fuel);
            System.out.println("상태: " + this.condition);
            System.out.println("주유가 필요가 필요합니다.\n");
        }
        if (this.fuel < 0){
            System.out.println("잘못 입력하셨습니다.\n");
        }
    }
    @Override
    public void changeCondition(String inputCondition) {
        if ("차고지행".equals(inputCondition)||("운행".equals(inputCondition) || "운행중".equals(inputCondition))) {
            this.condition = inputCondition;
        } else{
            System.out.println("잘못 입력하셨습니다.\n\n");
        }
    }
//      승객탑승

    void getPassenger(int a) {
        if ("운행".equals(this.condition) || "운행중".equals(this.condition)) {
            if (this.maxPassenger - a > 0) {
                this.maxPassenger -= a;
                this.currentPassenger += a;
                System.out.printf("탑승 승객 수: %d\n", a);
                System.out.printf("현재 탑승 중인 승객 수: %d\n", this.currentPassenger);  // 추가 된 부분
                System.out.printf("잔여 승객 수: %d\n", this.maxPassenger);
                System.out.printf("요금 : %d\n\n", a * price);
            } else {
                System.out.println("\t최대 승객 수 초과\n\n");
            }
        } else {
            this.condition = "차고지행";
            System.out.println(this.condition + "\n탑승 불가능합니다.");

        }
    }


}
